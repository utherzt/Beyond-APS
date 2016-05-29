### Terms

---

**`Database`**: A collection of interrelated stored data and description of data.

- why need database

  Usually data is too large to fit into main memory, and often used by many users.

---

**`DBMS`**: DBMS is short for `Database Management SYstem`, a software system designed to store, manage, and facilitate access to databases.

---

**`Data Model`**: A `Data Model` is a collection of concepts for describing data.

---

**`Schema`**: A `Schema` is a description of a particular collection of data, using a given data model.

---

**`Relational Model of Data`**: The `relational model of data` is the most widely used model today.

- Main Concept: `relation`, basically a table with rows and columns.

- Every relation has a schema, which describes the columns(fields, attributes) and keys.

---

**`ER model`**: entities & relationships

- Entity: Real-world object distinguishable from other objects. An entity is described in DB using a set of attributes. (e.g. of Web search: words, documents)

  - Entity Set: A collection of similar entities. E.g., all employees.

    - All entities in entity set have same set of attributes.

    - Each entity set has a key.

    - Each attribute has a domain.

- Relationship: Association among two or more entities. (e.g. of Web Search: word in document, document links to document)
  - Relationship Set: Collection of similar relationships. Same entity set could participate in different relationship sets ('roles') in the same set.

---

**`Relational Database`**: a set of relations.

详细解释: A relational database is a collection of data items organized as a set of formally described tables from which data can be accessed easily. A relational database is created using the relational model 关系模型. The software used in a relational database is called a relational database management system (RDBMS).

A relation is defined as a set of tuples 元组 that have the same attributes. A tuple usually represents an object and information about that object. Objects are typically physical objects or concepts. A relation is usually described as a table, which is organized into rows and columns. All the data referenced by an attribute are in the same domain and conform to the same constraints.

The relational model specifies that the tuples of a relation have no specific order and that the tuples, in turn, impose no order on the attributes. Applications access data by specifying queries, which use operations such as select to identify tuples, project to identify attributes, and join to combine relations. Relations can be modified using the insert, delete, and update operators. New tuples can supply explicit values 确定值 or be derived from a query. Similarly, queries identify tuples for updating or deleting. It is necessary for each tuple of a relation to be uniquely identifiable by some combination (one or more) of its attribute values.


- Relation: made up of 2 parts -- Instance and schema.

    - Instance: A table, with rows (tuples) and columns (attributes).

    - Schema: specifies name of relations, plus name and type of each column.

- Super Key

  A super key is any combination of columns that uniquely identifies a row in a table.

- Candidate Key

    A candidate key is a super key which cannot have any columns removed from it without losing the unique identification property.

- Primary key

    The candidate key that chosen by database designer to identify uniquely an entity.

- Foreign Key

    A attribute that is the primary key of another relation schema.

- Index

    A database index is a data structure that improves the speed of data retrieval operations on a database table at the cost of additional writes and storage space to maintain the index data structure.

---

**`Transaction`**: an sequence of database actions (reads/writes) executed atomically by DBMS. should take DB from one consistent state to another.

---

**`DDL`**: Data Definition Language

---

**`DML`**: Data Manipulation Language = query language (e.g. SQL)

---

**`DCL`**: Data Control Language

---

**`SQL`**: Structured Query Language  is a special-purpose programming language designed for managing data held in a relational database management system (RDBMS), or for stream processing in a relational data stream management system (RDSMS).

---

**`View`**: Views can be used to present necessary information (or provide a summary), while hiding details in underlying relation(s).
