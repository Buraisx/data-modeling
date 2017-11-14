 1.	
+--------------+ +--------------+
|    Customer  | | Order        |
+--------------+ +--------------+
| id           |-> customer_id  |
| name         | | order_num    |
| email        | | date         |
| address      | |              |
+--------------+ +--------------+

 2. 
 +----------------+  +-------------+  +--------------+   +------------+  +--------------+
| Country        |  | Province    |  |City          |   | Residence  |  | Person       |
+----------------+  +-------------+  +--------------+   +------------+  +--------------+
| name           ++ | name        ++ |name          +-+ | address    ++ | name         |
| yea_founded    || | year_founded|| |year_founded  | | | year_built || | age          |
| national_animal|+-> country     |+->province      | +-> city       |+-> res_address  |
|                |  |             |  |              |   |            |  | person_id    |
+----------------+  +-------------+  +--------------+   +------------+  +--------------+

3.  
+-----------+       +----------------+    +--------------+   +-----------+
|  Author   |       |  Book          |    | Hold         |   | Patreon   |
+-----------+       +----------------+    +--------------+   +-----------+
| name      |       |  title         |    | date_placed  |   | name      |
| id        +----+  |  isbn          |  +-> book_id      |   | card_num  |
|           |    +-->  author_id     |  | | patreon_id   <-+ | email     |
+-----------+       |  book_id       +--+ |              | +-+ patreon_id|
                    |                |    +--------------+   +-----------+
                    +-----------+----+                       |
                                |                            |
                                |         +---------------+  |
                                |         |Loan           |  |
                                |         +---------------+  |
                                |         | due_date      |  |
                                |         | renewed       |  |
                                +---------> book_id       |  |
                                          | patreon_id    <--+
                                          |               |
                                          +---------------+
