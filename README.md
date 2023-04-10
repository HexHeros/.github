# CS340 Project Guide
The CS340 Project that you will submit at the end of this course should satisfy all these specifications:

- Your database should be pre-populated with sample data. At least three rows per table is expected. The sample data should illustrate a table's functionality, e.g. if the table is part of a many-to-many relationship, the sample data should depict M:M.
- Your database should have at least 4 entities and at least 4 relationships, one of which must be a many-to-many relationship.  The entities and relationships should implement the operational requirements of your project.
- You are creating a web interface for data tables, so the primary user is the administrator of this database.
  - It is NOT a customer facing website; thus there is no need for login page; sessions; register/password; shopping cart; check-out; etc.  While having those pages would be helpful in many customer facing applications, the purpose of this project is to provide a UI for your tables. 
   - Put another way, if you had 4 entities that were implemented as 5 tables in a database, then we expect roughly 5 web app pages as a front end UX for each of the 5 tables in your database.
    - One exception is oftentimes it works better for the UX to have a single web page for a Many-to-Many relationship between 2 tables (so the user doesn't have to view two pages to complete a transaction in both tables). So in that case if you had 4 entities that were implemented as 5 tables, with 1 many-to-many relationship between 2 of those tables, and the 2 tables in that m:m were managed on a single web page, then we expect 4 web pages in the project. 
    - Some students may choose to add a home page to their project, which is acceptable but not required. To continue the example from the previous item, adding a home page would be a 5th page in the project. 
- It should be possible to `INSERT` entries into every table individually.
- Every table should be used in at least one `SELECT` query. For the `SELECT` queries, it is fine to just display the content of the tables. It is generally not appropriate to have only a single query that joins all tables and displays them.
- You need to include one `DELETE` and one `UPDATE` function in your website, for any one of the entities. In addition, it should be possible to add and remove things from at least one many-to-many relationship and it should be possible to add things to all relationships. This means you need `SELECT` & `INSERT` functionalities for all relationships as well as entities. And `DELETE` & `UPDATE` for least one m:m relationship.
- Note that it's not acceptable to require the user to enter IDs for foreign keys. Instead your website needs to use a dynamically populated drop-down list or have the ability to search using text instead of entering in the ID. This Dynamic drop-down/Search functionality should be present for at least one entity. 
- In one relationship, you should be able to set the foreign key value to `NULL` using `UPDATE`, that removes the relationship. In case none of the one-to-many relationships in your database has optional participation, you would need to change that to make sure one can have NULL values. For example, in the table Orders, there may be two FKs: the employeeID and the customerID which create relations to the Employees and Customers tables. It may not be sensible for the Customer to be optional. But the Employee could be optional. Thus, we would expect that in the Orders `INSERT` and `UPDATE` pages it is possible to set the employeeID to a value or else to `NULL`. 
- You should be able to `DELETE` a record from a M:M relationship without creating a data anomaly in the related tables. For example, `DELETE`ing a Customer should handle any Orders that were made by the Customer. This can be done by either by setting the CustomerID to `NULL`, or else by `DELETE`ing any Order(s) associated with that Customer. More on how this can be done in Week 5 when we cover MySQL CASCADE. 
- To continue the example from above, if you have 5 tables in your schema, then at a minimum, we expect you to implement 5 `SELECT`s, 5 `INSERT`s, 1 `UPDATE` (1 `NULL`able relationship), 1 `DELETE` (M:M), and 1 Dynamic drop-down/Search for a total of 14 functions. 
 

## General Rules and Grading
- Can be developed using any technology platform which serves content over the web.
- Should use an SQL driven database back end (e.g. MySQL/MariaDB, PostgreSQL, MSSQL, etc.).
- You should write all the queries and not depend on an ORM or similar mechanism to generate any queries.
- You can host it anywhere as long as it is accessible to the graders.
- You are required to work on the Project Steps in a Project Group of two students. By the end of Week 1, you are required to submit the names of your team members. It’s recommended that you have a set weekly meeting time to check on the progress and also use tools like version control to keep in sync. You can change groups at most 1 time through the quarter, and then only if you find someone else ready to swap groups.
- Please note that the CS340 database created for you will be deleted from the server at the end of the term.
- You will be working on this project over several weeks, earning points for each step completed.

