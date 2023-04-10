# 2⃣ Relational DB & Design

#### MLO's

* Model a moderately complex data set by using an ER  diagram, and derive a relational schema from that diagram
* Explain various terminologies used when talking about relational databases&#x20;
* Explain the various kinds of relationships that entities can participate in
* Use the Crow's foot notation&#x20;
* Complete all activities and assignments

## Database Design Patterns

Relational databases store data in two-dimensional table by using foreign keys to support one-to-many relationships that commonly occur in organizational data. Foreign keys nicely support relationships and reduce common problems (data anomalies) associated with poor design. Fortunately, there are common database design patterns that can be used to classify most tables in a schema of typical complexity.

#### Vocabulary

* Database - a collection of data and metadata about the structure of relationships, it serves many applications efficiently by centralizing the data and controlling redundant data.
* Database management system (DBMS)software that permits an organization to centralize data, manage them efficiently, and provide access to the stored data by application programs.Transaction processing databases handle the day‐to‐day operations of an organization.
* Entity - a person or place or thing (object), or event (transaction) on which we store and maintain information.
* Schema - describes a **Logical View** of a database structure not a physical view Tables, Tuples, Attributes, and Keys are key parts of a database schema.
* Normalization - creates small, stable, flexible, and adaptive data structures for complex groups of data. It emphasizes creating separate tables for separate entities.
  * The goal of normalization is to prevent **Data redundancy and data anomalies**.
* **Data redundancy** exists when unnecessarily duplicated data are found in the database and illustrates poor database design. For example, a customer's telephone number may be found in the customer file and in the invoice file. Data redundancy is symptomatic of a (computer) file system, given its inability to represent and manage data relationships. It also contributes to **update anomalies** –the problem when data is changed in one place but not another.
  * Another common problem of poor data design is **insert anomalies**, for example if it is not possible to add a customer without first having an invoice then we would have to create a dummy invoice, which is a poor design. Similarly **delete anomalies** occur when deleting information about one entity also deletes another. So in the previous example, if deleting an invoice also deleted the customer data that would also be an example of poor design.
* Attributes - specific characteristics of entities. The smallest unit of data with meaning to a user; columns, fields&#x20;
* Relationships- describes an association between entities. Examples include a one‐to‐many (1:M), many to many (M:M or M:N) and a one‐to‐one (1:1)TableEach type of entity or event gets its own table (aka. a relation)
* Record- a **row** in a table ‐ corresponds to one item e.g., each customer has its own record (aka. **Tuple**)
* Cardinality - the number of items in one table that correspond, over time, to one item in the related table
  * Primary KeyAn attribute (or combination of attributes) that uniquely identifies a row
  * Foreign KeyA field in one table that refers to the primary key of another – a lookup field
* Referential Integrity - Rules that enforce defined relationships between tables ‐ If you refer to a row in another table, it has to actually exist. DBMS systems can easily prevent adding a product to an invoice if that product does not actually exist in the products table
* **Summary data** are attributes stored in an object table that are effected by transactions. These are also referred to as calculated data. They are computed by a program or a query and then stored in the table. For example total\_sales might be an attribute stored in a customer table.

\
