### Normal Form (IMPORTANT)

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
