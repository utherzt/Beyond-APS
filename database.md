## <a name="database"></a>Database Principles and Design

### <a name="database-introduction"></a>Course Introduction

---

### <a name="database-terms"></a>Terms

**`Database`**: A collection of interrelated stored data and description of data.

- why need database

  Usually data is too large to fit into main memory, and often used by many users.

**`DBMS`**: DBMS is short for `Database Management SYstem`, a software system designed to store, manage, and facilitate access to databases.

**`Data Model`**: A `Data Model` is a collection of concepts for describing data.

**`Schema`**: A `Schema` is a description of a particular collection of data, using a given data model.

**`Relational Model of Data`**: The `relational model of data` is the most widely used model today.

- Main Concept: `relation`, basically a table with rows and columns.

- Every relation has a schema, which describes the columns(fields, attributes) and keys.

**`ER model`**: entities & relationships

- Entity: Real-world object distinguishable from other objects. An entity is described in DB using a set of attributes. (e.g. of Web search: words, documents)

  - Entity Set: A collection of similar entities. E.g., all employees.

    - All entities in entity set have same set of attributes.

    - Each entity set has a key.

    - Each attribute has a domain.

- Relationship: Association among two or more entities. (e.g. of Web Search: word in document, document links to document)
  - Relationship Set: Collection of similar relationships. Same entity set could participate in different relationship sets ('roles') in the same set.

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

    加快查找对应数值的速度。索引会对字段排序，查找某条记录时先在索引找到匹配值,然后再在Table中返回对应行的记录


**`Transaction`**: an sequence of database actions (reads/writes) executed atomically by DBMS. should take DB from one consistent state to another.

**`DDL`**: Data Definition Language

**`DML`**: Data Manipulation Language = query language (e.g. SQL)

**`DCL`**: Data Control Language

**`SQL`**: Structured Query Language  is a special-purpose programming language designed for managing data held in a relational database management system (RDBMS), or for stream processing in a relational data stream management system (RDSMS).

**`View`**: Views can be used to present necessary information (or provide a summary), while hiding details in underlying relation(s).

---

### <a name="database-three-schema"></a>Three-Schema Architecture

#### Internal Schema

Describes the physical storage structure of a database.

#### Conceptual Schema

Describes the whole structure of a database to users.

#### External Schema

Describes a part of a database, in which a group of users are interested other parts are hidden from these users for example.

---

### <a name="database-sql"></a>SQL

Reference:[W3Schools SQL Tutorial](http://www.w3schools.com/sql/)

---

### <a name="database-constraints"></a>Constraints

`NOT NULL Constraint`:

`UNIQUE Constraint`:

`PRIMARY KEY Constraint`:

`Foreign Key Constraint`:

`Check Constraint`:

---

### <a name="database-normal-form"></a>Normal Form (IMPORTANT)

Reference: [Normalization of Database](http://www.studytonight.com/dbms/database-normalization.php)

#### 1NF

Reference: [WikiPedia 1NF](https://en.wikipedia.org/wiki/First_normal_form)

The domain of each attribute contains only atomic values, and the value of each attribute contains only a single value from that domain.
Every line has and only has one instance of entity. This Normal form is required for relationship DB

#### 2NF

Reference: [WikiPedia 2NF](https://en.wikipedia.org/wiki/Second_normal_form)

Every non-prime attribute in the table is functionally dependent on a proper subset of any candidate key

#### 3NF

Reference: [WikiPedia 3NF](https://en.wikipedia.org/wiki/Third_normal_form)

Every non-prime attribute is non-transitively dependent on every candidate key in the table, no transitive dependency is allowed.

#### BCNF

Reference: [WikiPedia BCNF](https://en.wikipedia.org/wiki/Boyce–Codd_normal_form)

Every non-trivial functional dependency in the table is a dependency on a super key

---

### <a name="database-relational-model>Relational Model(Example)


---

### <a name="database-er-diagram"></a>ER Diagram

ER Diagram is short for Entity-Relationship Diagram, describe the attributes of entities and the relationship among entities.

translate entity to tables

translate relationships to tables

---

### <a name="database-how-to"></a>How to Design a Database (IMPORTANT)

1. Requirements Analysis

- user needs; what must database do?

2. Conceptual Design

- high level description (often done w/ER model)

- Rails encourages you to work here

3. Logical Design

- translate ER into DBMS data model

- Rails requires you to work here too

4. Schema Refinement

- consistency, normalization

5. Physical Design

- indexes, disk layout

6. Security Design

- who accesses what, and how

---

### <a name="database-practical-application"></a>Practical Application
