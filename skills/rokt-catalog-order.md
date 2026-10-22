---
name: rokt-catalog-order
description: Browse Rokt Catalog products, quote shipping and tax, place an order idempotently, and track fulfillment.
api: openapi/rokt-catalog-api-openapi.yml
operations:
  - products_list
  - variants_list
  - tax_and_shipping_calculate_create
  - orders_create_or_get_create
  - orders_retrieve
  - fulfillments_list
  - orders_cancel_create
generated: 2026-10-21
method: generated
---
# Rokt Catalog API: storefront order flow

Server: `https://api.shopcanal.com/platform`. Rokt Catalog was formerly Canal, and the spec still uses that host. Auth: the `X-CANAL-APP-ID` and `X-CANAL-APP-TOKEN` headers, from Settings > API Credentials. Keep the token server-side.

1. `products_list` and `variants_list`: find the items to sell.
2. `tax_and_shipping_calculate_create`: quote tax and shipping for the cart.
3. `orders_create_or_get_create`: create the order keyed on your storefront's `order_name`. The spec says this is the idempotent path, so prefer it over `orders_create`.
4. `orders_retrieve` and `fulfillments_list`: track the order.
5. If needed, `orders_cancel_create` cancels the order.
