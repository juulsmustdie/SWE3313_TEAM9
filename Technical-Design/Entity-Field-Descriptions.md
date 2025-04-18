User

| **Property** | Type | Default | Nullable | Relationship | Notes |
| --- | --- | --- | --- | --- | --- |
| user_id | Primary key, integer, identity |  |  | Relate to Cart.user_id and Order.user_id |  |
| is_admin | boolean |  |  |  |  |
| name | varchar100 |  |  |  | only for admins |
| email | varchar100 |  |  |  | only for admins |
| password | varchar100 |  |  |  | only for admins |
