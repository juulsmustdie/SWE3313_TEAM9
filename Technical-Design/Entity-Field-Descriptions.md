## User

| **Property** | Type | Default | Nullable | Relationship | Notes |
| --- | --- | --- | --- | --- | --- |
| user_id | Primary key, integer, identity |  | No | Relate to Cart.user_id and Order.user_id |  |
| is_admin | Boolean | False | No |  |  |
| name | String(50) | “” | Yes |  | Null for users, required for admins |
| email | String(100) | “” | Yes |  | Null for users, required for admins |
| password | String(255) | “” | Yes |  | Null for users, required for admins |

## Product

| **Property** | Type | Default | Nullable | Relationship | Notes |
| --- | --- | --- | --- | --- | --- |
| product_id | Primary key, integer, identity |  | No | Relate to Cart_item.product_id and Orderline.product_id |  |
| name | String(100) | “” | No |  |  |
| current_price | Float | 0.0 | No |  |  |
| description | String(300) | “” | No |  |  |
| in_stock | Boolean | True | No |  |  |
| picture | String(255) |  | No |  | file path to image |

## Cart

| **Property** | Type | Default | Nullable | Relationship | Notes |
| --- | --- | --- | --- | --- | --- |
| cart_id | Primary key, integer, identity |  | No | Relate to Cart_item.cart_id |  |
| user_id | Foreign key, integer |  | No | Relate to User.user_id |  |

## Cart_item

| **Property** | Type | Default | Nullable | Relationship | Notes |
| --- | --- | --- | --- | --- | --- |
| cart_item_id | Primary key, integer, identity |  | No |  |  |
| cart_id | Foreign key, integer |  | No | Relate to Cart.cart_id |  |
| product_id | Foreign key, integer |  | No | Relate to Product.product_id |  |

## Order

| **Property** | Type | Default | Nullable | Relationship | Notes |
| --- | --- | --- | --- | --- | --- |
| order_id | Primary key, integer, identity |  | No | Relate to Orderline.order_id |  |
| user_id | Foreign key, integer |  | No | Relate to User.user_id |  |
| order_date | DateTime | now() | No |  |  |
| subtotal | Float | 0.0 | No |  |  |
| tax | Float | 0.0 | No |  |  |
| total | Float | 0.0 | No |  |  |

## Orderline

| **Property** | Type | Default | Nullable | Relationship | Notes |
| --- | --- | --- | --- | --- | --- |
| orderline_id | Primary key, integer, identity |  | No |  |  |
| order_id | Foreign key, integer |  | No | Relate to Order.order_id |  |
| product_id | Foreign key, integer |  | No | Relate to Product.product_id |  |
| purchase_price | Float | 0.0 | No |  |  |
