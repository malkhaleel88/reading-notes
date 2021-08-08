# **Mongo and Mongoose**

## **nosql vs sql**


 ### **Fill in the chart below with five differences between SQL and NoSQL databases:**

            |        **SQL**           |           **NoSQL**        |
            | ------------------------ | -------------------------- |
            | Relational Databases     | Non-relational or Distributed database |
            | Table based databases    | document based |
            |  Predefined schema | Dynamic schema |
            | Vertically scalable | Horizontally scalable |
            | Emphasizes on ACID properties  | Follows the Brewers CAP theorem |
            | Not best fit for hierarchical data storage | Better for the hierarchical data storage |

 ### **What kind of data is a good fit for an SQL database?**

 *If your data is highly structured and associations among the program entities are clearly defined (for instance, if you are developing a point of sale system where you need to store customer orders and product records)*

 ### **Give a real world example.

 *MySQL database is very popular open-source database. It is generally been stacked with apache and PHP, although it can be also stacked with nginx and server side javascripting using Node js.*

 ### **What kind of data is a good fit a NoSQL database?**

 * Fits better for the hierarchical data storage as it follows the key-value pair way of storing data similar to JSON data. NoSQL database are highly preferred for large data set (i.e for big data). Hbase is an example for this purpose.*

 ### **Give a real world example.**

 *Mongodb is one of the most popular document based NoSQL database as it stores data in JSON like documents. It is non-relational database with dynamic schema. It has been developed by the founders of DoubleClick, written in C++ and is currently being used by some big companies like The New York Times, Craigslist, MTV Networks.*

 ### **Which type of database is best for hierarchical data storage?**

 *NoSQL*

 ### **Which type of database is best for scalability?**

 *NoSQL*

 ### **What does SQL stand for?**

 *Structured Query Language*

 ### **What is a realational database?**

 *Database which works with certain assumptions or in certain way*

 ### **What type of structure does a relational database work with?**

 *This model organizes data into one or more tables (or "relations") of columns and rows, with a unique key identifying each row. *

 ### **What is a ‘schema’?**

 *How database table looks like in a sql*

 ### **What is a NoSQL database?**

 *Non tabular, and store data differently than relational tables. NoSQL databases come in a variety of types based on their data model. The main types are document, key-value, wide-column, and graph. They provide flexible schemas and scale easily with large amounts of data and high user loads.*

 ### **How does it work?**

 *A MongoDB Collection is simply made of Documents along with some index definitions. The documents are all basically JSON objects: i.e.: hashtables. Each document has the full definition of everything in it. There are no "column names" and there is no restrictions on what goes in. So if put a "User" document in the same collection as a "OrderDetails" document, the DB does not really care.*

 ### **What is inside of a Mongo database?**

 *MongoDB stores data records as documents (specifically BSON documents) which are gathered together in collections. A database stores one or more collections of documents.*

 ### **Which is more flexible - SQL or MongoDB? and why.**

 *MongoDB, These databases provide flexibility for data that has not been normalized, which requires a flexible data model, or has different properties for different data entities.*

 ### **What is the disadvantage of a NoSQL database?**

 * Each NoSQL database has its own syntax for querying and managing data. This is in contrast to SQL, which is the lingua franca for relational and SQL database systems.
 * Lack of a rigid database schema and constraints removes the data integrity safeguards that are built into relational and SQL database systems.
 * A schema with some sort of structure is required in order to use the data. With NoSQL, this must be performed by the application developer instead of the database administrator.
 * Because most NoSQL databases use the eventual consistency model, they do not provide the same level of data consistency as SQL databases. At times the data will not be consistent, which means they are not well-suited for transactions that require immediate integrity, such as banking and ATM transactions.
 * Because NoSQL databases are newer, there are no comprehensive industry standards as with relational and SQL DBMS offerings. 



 ## **Things I want to know more about**



[HOME](https://malkhaleel88.github.io/reading-notes)

