# [SQL](https://en.wikipedia.org/wiki/SQL) ([Relational](https://en.wikipedia.org/wiki/Relational_database))

## [Relational Data Model](https://en.wikipedia.org/wiki/Relational_model)

Guru99 provides a [brief explination](https://www.guru99.com/relational-data-model-dbms.html) for the relational model.  
![Relational Data Model Example](/Relational_Data_Model_Example.png)

### [Concepts:](https://www.tutorialspoint.com/dbms/relational_data_model.htm)

- **Logical Schema (Constraints)**: A logical representation of information enforced by declared constraints.
- **Attribute**: A column in a Table. Consists of an attribute (column) name and type name.
- **Tables**: All data is stored in tables. A table is made up of rows (records) and columns (attributes).
- **Tuple**: A single row of a table, which contains a single record.
- **Degree**: The total number of attributes in the relation.
- **Cardinality**: Total number of rows present in the Table.
- **Column**: The column represents the set of values for a specific attribute.
- **Relation instance**: A finite set of tuples in the RDBMS system. Relation instances never have duplicate tuples.
- **Relation Schema**: A relation schema represents the relation name (schema) with its attributes and their names.
- **Relation key**: Every row has one or more which can identify a row in the relation table.
- **Attribute domain**: The set of values allowed in an attribute.

### [Normalization](https://en.wikipedia.org/wiki/Database_normalization)

The goal of normalization is to remove data redundancy in the database, typically by utilizing a relational model. Its objective is to remove update, insertion, and deletion anomalies. Each value should only exist in one location with its relevant related attributes to be simply maintained in one location. Most applications will be best achieved following [third normal form (3NF)](https://en.wikipedia.org/wiki/Third_normal_form).

### [Denormalization](https://en.wikipedia.org/wiki/Denormalization)

Denormalization is a strategy to improve the read performance of a database, at the expense of some write performance, by adding redundant data or grouping data.

**Denormalization techniques:**

- "Storing" the count of the "many" elements in a one-to-many relationship as an attribute of the "one" relation
- Adding attributes to a relation from another relation with which it will be joined
- [Star schemas](https://en.wikipedia.org/wiki/Star_schema), which are also known as fact-dimension models and have been extended to [snowflake schemas](https://en.wikipedia.org/wiki/Snowflake_schema)
- Prebuilt summarization or OLAP cubes

<br>

## [MySQL](https://www.mysql.com/)

An open source Relational Database Management System (RDBMS). Cloud deployment is available through [Microsoft Azure](https://azure.microsoft.com/en-gb/services/mysql/), [Amazon AWS](https://aws.amazon.com/rds/mysql/), and [Oracle Cloud](https://cloud.oracle.com/en_US/infrastructure/compute).

## Queries

[SQL Tutorial on w3schools.com](https://www.w3schools.com/sql/sql_intro.asp)

**What it can do:**

- Retrieve data from a database
- Insert records in a database
- Update records in a database
- Delete records from a database
- Create new databases
- Create new tables in a database
- Create stored procedures in a database
- Create views in a database
- Set permissions on tables, procedures, and views

<br>

# [NoSQL (Non-Relational)](https://en.wikipedia.org/wiki/NoSQL)

NoSQL databases are increasing in popularity with [big data](https://en.wikipedia.org/wiki/Big_data) and real-time web applications. NoSQL databases offer advantages with simple implementation, friendly data design, and cost efficient scaling. NoSQL databases add servers to scale instead of increasing processing power with SQL databases. NoSQL databases forefit atomic (all-or-nothing) writes to the database available with a SQL DB.

## [Document-oriented](https://en.wikipedia.org/wiki/Document-oriented_database)

Documents use object notation with key-value store. Common encodings are [XML](https://en.wikipedia.org/wiki/XML), [YAML](https://en.wikipedia.org/wiki/YAML), [JSON](https://en.wikipedia.org/wiki/JSON), and [BSON](https://en.wikipedia.org/wiki/BSON). Documents in a store can be of different types since they are not required to adhere to a standard schema. Documents are also able to offer optional fields.

### Concepts

- **Core operations (CRUD)**
  - **Creation** (Insertion)
  - **Retrieval** (Query, search, read, or find)
  - **Update** (edit)
  - **Deletion** (removal)
- **Keys**: Simple identifier. Typically a string, URI, or path.
- **Retrieval**: Key-to-document lookup available as well as an API for content or metadata retrieval.
- **Editing**: Key or document replacement available.
- **Organization**
  - **Collections**: Groups of documents. A document may exist in one or more collections.
  - **Tags & non-visible metadata**: Data stored outside of the document's context
  - **Directory hierarchy**: Documents organized in tree-like structure, typically based on path or URI.

### [Firebase Cloud Firestore]()

- [Data Model](https://firebase.google.com/docs/firestore/data-model)
- [Querying](https://firebase.google.com/docs/firestore/query-data/queries)

### [MongoDB](https://www.mongodb.com/)

- [Data Model](https://docs.mongodb.com/manual/core/data-modeling-introduction/)
- [Querying](https://docs.mongodb.com/manual/tutorial/query-documents/)

<br>

## JSON Tree

### Concept

When you add data to the [JSON](https://en.wikipedia.org/wiki/JSON) tree, it becomes a node in the existing JSON structure with an associated key.

### Best practices

- Avoid nesting data
- Flatten data structures
- Create data that scales

### [Firebase Realtime Database](https://firebase.google.com/docs/database)

- [Data Model](https://firebase.google.com/docs/database/web/structure-data)
- [Querying](https://firebase.google.com/docs/database/web/lists-of-data#sorting_and_filtering_data)

<br>

## NoSQL Tabular

### [Concepts](https://www.tutorialspoint.com/cassandra/cassandra_architecture.htm)

- **Distributed database**: The database is spread across a cluster of nodes, data needs to be spread evenly amongst all participating nodes.
- **Data partitioning**: Distributing data across nodes.
- **Partition**: Groups of columns that share the same partition key.
- **Row key (partition key)**: responsible for determining data distribution across a cluster.
- **Data replication**: Due to the cluster architecture, data needs to be replicated across multiple nodes to avoid a single point of failure.
- **Keyspace**: Specify a replication strategy for the data and nodes.

### Best practices

- Spread data evenly around cluster
- Minimize number of partitions read
- Model around queries

### [Cassandra](https://cassandra.apache.org/)

"Cassandra is a distributed database from Apache that is highly scalable and designed to manage very large amounts of structured data. It provides high availability with no single point of failure."

- [Cassandra Query Language (CQL)](https://cassandra.apache.org/doc/latest/cql/)

<!-- Add time series db, APIs, and AWS resources -->
