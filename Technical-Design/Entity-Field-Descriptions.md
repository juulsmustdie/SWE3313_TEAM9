User

| **Property** | Type | Default | Nullable | Relationship | Notes |
| --- | --- | --- | --- | --- | --- |
| user_id | Primary key, integer, identity |  |  | Relate to Cart.user_id and Order.user_id |  |
| is_admin | boolean |  |  |  |  |
| name | varchar100 |  |  |  | only for admins |
| email | varchar100 |  |  |  | only for admins |
| password | varchar100 |  |  |  | only for admins |

Product

| **Property** | Type | Default | Nullable | Relationship | Notes |
| --- | --- | --- | --- | --- | --- |
| product_id | Primary key, integer, identity |  |  | Relate to Cart_item.product_id and Orderline.product_id |  |
| name | varchar100 |  |  |  |  |
| current_price | float |  |  |  |  |
| description | varchar100 |  |  |  |  |
| in_stock | boolean |  |  |  |  |

Cart

| **Property** | Type | Default | Nullable | Relationship | Notes |
| --- | --- | --- | --- | --- | --- |
| cart_id | Primary key, integer, identity |  |  | Relate to Cart_item.cart_id |  |
| user_id | Foreign key, integer |  |  | Relate to User.user_id |  |

Cart_item

| **Property** | Type | Default | Nullable | Relationship | Notes |
| --- | --- | --- | --- | --- | --- |
| cart_item_id | Primary key, integer, identity |  |  |  |  |
| cart_id | Foreign key, integer |  |  | Relate to Cart.cart_id |  |
| product_id | Foreign key, integer |  |  | Relate to Product.product_id |  |

Order

| **Property** | Type | Default | Nullable | Relationship | Notes |
| --- | --- | --- | --- | --- | --- |
| order_id | Primary key, integer, identity |  |  | Relate to Orderline.order_id |  |
| user_id | Foreign key, integer |  |  | Relate to User.user_id |  |
| order_date | varchar100 |  |  |  |  |
| subtotal | float |  |  |  |  |
| tax | float |  |  |  |  |
| total | float |  |  |  |  |

Orderline

| **Property** | Type | Default | Nullable | Relationship | Notes |
| --- | --- | --- | --- | --- | --- |
| orderline_id | Primary key, integer, identity |  |  |  |  |
| order_id | Foreign key, integer |  |  | Relate to Order.order_id |  |
| product_id | Foreign key, integer |  |  | Relate to Product.product_id |  |
| purchase_price | float |  |  |  |  |
