1. Explain the relationship between the "Product" and "Product_Category" entities from the above diagram.
   
The relationship between the "Product" and "Product_Category" entities in the diagram described is one-to-many.
A product can belong to one product category. This is indicated by the foreign key category_id in the "Product" table. The category_id column references the primary key (id) of the "Product_Category" table.
A product category can have many products. This is because there is no foreign key referencing the "Product" table in the "Product_Category" table.

3. How could you ensure that each product in the "Product" table has a valid category assigned to it?
   
This approach sets up a rule within the database itself. The foreign key constraint on the category_id column in the "Product" table verifies that the category ID of a product actually exists in the "Product_Category" table. This prevents invalid entries and guarantees data integrity.
While application logic validation can also check for valid categories during product addition or update, it relies on code implementation and doesn't offer the same level of automated enforcement as a database constraint.
