## User Entity

| user_id (PK) | name        | password        | email                   | is_admin |
| ------------ | ----------- | --------------- | ----------------------- | -------- |
| 1            | jeff@KSU    | prof_123        | jeff@ksu.prof.com       | yes      |
| 2            | julissa@KSU | catsRcool-456   | julissa@ksu.student.com | yes      |
| 3            | josh@KSU    | whatsKraken098! | josh@ksu.student.com    | yes      |
| 4            | andres@KSU  | ATisme!531!     | andres@ksu.student.com  | no       |
| 5            | tate@KSU    | fun4Me-_-4321   | tate@ksu.student.com    | yes      |



## Product Entity



| product_id (PK) | name                       | description                                                  | current_price (USD) | in_stock |
| :-------------- | -------------------------- | ------------------------------------------------------------ | ------------------- | -------- |
| 1               | Bronze Banana Blast        | banana cordial, caramel syrup, 2 shots espresso, milk, blended and topped with 						caramelized bananas | 9.99                | Yes      |
| 2               | Salted Caramel Mocha       | shots espresso, salted caramel syrup, non-alcoholic chocolate bitters, milk, topped with shaved dark chocolate | 7.99                | Yes      |
| 3               | Very Berry Hibiscus Cooler | blackberries, blueberries, and mint muddled in a shaker, with agave, shaken and topped with sparkling water and garnished with fresh mint | 8.50                | No       |
| 4               | Honey Lavender Espresso    | Lavender syrup, honey, 2 shots espresso, milk                | 4.79                | Yes      |
| 5               | Pistachio Cardamom Roll    | cardamom and pistachio baked into a house-made brioche roll, topped with shaved pistachios | 6.50                | No       |
| 6               | Truly Blue Tiramisu        | traditional tiramisu base, with fresh espresso and blueberry syrup incorporated. Topped with blueberry compote and an Oreo crust | 12.99               | Yes      |





## Order Entity

| user_id (FK) | order_id (PK) | order_date | subtotal | tax  | total |
| ------------ | ------------- | ---------- | -------- | ---- | ----- |
| 1            | 4             | 04/09/25   | 19.99    | 1.40 | 21.39 |
| 3            | 3             | 04/01/25   | 26.79    | 1.88 | 28.67 |
| 4            | 5             | 02/04/25   | 4.79     | 0.34 | 5.13  |
| 5            | 2             | 04/16/25   | 11.29    | 0.79 | 12.08 |
| 2            | 1             | 03/29/25   | 25.98    | 1.82 | 27.80 |



## Cart

| cart_id (PK) | user_id (FK) |
| ------------ | ------------ |
| 1            | 4            |
| 2            | 2            |
| 3            | 3            |
| 4            | 5            |
| 5            | 1            |



## Cart Item

| cart_item_id (PK) | cart_id (FK) | product_id (FK) |
| ----------------- | ------------ | --------------- |
| 1                 | 5            | 3               |
| 2                 | 3            | 4               |
| 3                 | 2            | 5               |
| 4                 | 4            | 2               |
| 5                 | 1            | 1               |



## Orderline

| orderline_id (PK) | order_id (FK) | product_id (FK) | purchase_price |
| ----------------- | ------------- | --------------- | -------------- |
| 1                 | 5             | 3               | 8.50           |
| 2                 | 2             | 4               | 4.79           |
| 3                 | 3             | 5               | 12.99          |
| 4                 | 4             | 2               | 7.99           |
| 5                 | 1             | 1               | 9.99           |
