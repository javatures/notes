# Week 2 - SQL
# SQL
## Concepts
- RDBMS
- Sublanguages: DDL, DML, DQL
- Set Operators: Union, Intersect, Except
- Subqueries
- Normalization: 1st vs 2nd vs 3rd Normal Forms
- Multiplicity: Foreign keys
- Joins: Inner, Outer, Cross
- Functions: Aggregate vs Scalar

## Syntax
- [DDL](https://www.postgresql.org/docs/12/ddl.html): 
  - [CREATE TABLE](https://www.postgresql.org/docs/12/sql-createtable.html)
  - [ALTER TABLE](https://www.postgresql.org/docs/12/sql-altertable.html)
  - [DROP TABLE](https://www.postgresql.org/docs/12/sql-droptable.html)
- [DML](https://www.postgresql.org/docs/12/dml.html): 
  - [INSERT](https://www.postgresql.org/docs/12/sql-insert.html)
  - [UPDATE](https://www.postgresql.org/docs/12/sql-update.html)
  - [DELETE](https://www.postgresql.org/docs/12/sql-delete.html)
- [DQL](https://www.postgresql.org/docs/12/queries.html):
  - [SELECT](https://www.postgresql.org/docs/12/sql-select.html)
  - Combining Queries: [UNION/INTERSECT/EXCEPT](https://www.postgresql.org/docs/12/queries-union.html)
  - [Scalar Subqueries](https://www.postgresql.org/docs/12/sql-expressions.html#SQL-SYNTAX-SCALAR-SUBQUERIES)
  - [Subquery Expressions](https://www.postgresql.org/docs/12/functions-subquery.html)
  - [Joined Tables](https://www.postgresql.org/docs/12/queries-table-expressions.html#QUERIES-JOIN)
- [Functions](https://www.postgresql.org/docs/12/functions.html):
  - [Aggregate Functions](https://www.postgresql.org/docs/12/functions-aggregate.html)
  - Scalar Functions:
    - [Date/Time](https://www.postgresql.org/docs/12/functions-datetime.html)
    - [Math](https://www.postgresql.org/docs/12/functions-math.html)
    - [Strings](https://www.postgresql.org/docs/12/functions-string.html)

# JDBC
## Concepts
- [Java JDBC API](https://docs.oracle.com/javase/8/docs/technotes/guides/jdbc/)

## Standard Library
- [java.sql](https://docs.oracle.com/javase/8/docs/api/java/sql/package-summary.html)
  - [DriverManager](https://docs.oracle.com/javase/8/docs/api/java/sql/DriverManager.html)
  - [Connection](https://docs.oracle.com/javase/8/docs/api/java/sql/Connection.html)
  - [Statement](https://docs.oracle.com/javase/8/docs/api/java/sql/Statement.html)
    - [PreparedStatement](https://docs.oracle.com/javase/8/docs/api/java/sql/PreparedStatement.html)
    - [CallableStatement](https://docs.oracle.com/javase/8/docs/api/java/sql/CallableStatement.html)
  - [ResultSet](https://docs.oracle.com/javase/8/docs/api/java/sql/ResultSet.html)
  - [SQLException](https://docs.oracle.com/javase/8/docs/api/java/sql/SQLException.html)

# Questions
## SQL
- What is SQL?
- What are its sublanguages?
- What is multiplicity?
- What is cardinality?
- What is a candidate key?
- What is referential integrity?
- What are the different constraints of a column?
- what are the differences between GROUP BY and ORDER BY?
- What is the difference between IN and EXISTS?
- What are subqueries?
- What is the differenece between an aggregate function and a scalar function?
- What are the different joins in SQL?
- What are the different set operations in SQL?
- What is the difference between joins and set operations?
- What is normalization?
- What are the requirements for the first three normal forms?

## JDBC
- What is JDBC?
- What dependencies are required to connect to an RDBMS?
- What are the main interfaces of JDBC?
- In what order are they used?
- What are the different types of statements?
- What is SQL Injection?
- What is a DAO?
- Describe client-server communication: how does it apply to PostgreSQL?
- What does a connection URL for PostgreSQL look like?
- How do you connect to a PostgreSQL server with a client? With Java?
- Why is connection pooling important?

# PostgreSQL on Docker
Docker is a containerization tool written in Go to create lightweight containers running isolated file systems and processes. By downloading the official PostgreSQL docker image, we can run disposable database servers.

### Example: PostgreSQL Server
To run a simple Postgres server instance:
>docker run -e POSTGRES_PASSWORD password -p [port]:5432 postgres

Where [port] is your choice of port. A common port is 5432, a default for many Postgres databases:
>docker run -e POSTGRES_PASSWORD password -p 5432:5432 postgres

To run a database as a background process, use the `-d` switch:
>docker run -e POSTGRES_PASSWORD password -d -p 5432:5432 postgres

It's a good idea to label a database with the `--name` switch:
>docker run -e POSTGRES_PASSWORD password -d --name my_postgres -p 5432:5432 postgres

To see running containers, use:
>docker ps

To stop a container, run:
>docker stop <CONTAINER-NAME-OR-ID>

### Running PostgreSQL from a Dockerfile
To create a custom postgres database, create a file named `Dockerfile`:
```Dockerfile
FROM postgres:10
ENV POSTGRES_USER hello-postgres
ENV POSTGRES_PASSWORD hello-postgres
ADD init.sql /docker-entrypoint-initdb.d
EXPOSE 5432
```

Where init.sql is an optional `.sql` script file in the same directory as your Dockerfile. Use `ENV` to set the username and password as needed. Both `ENV` lines can be omitted, causing the username to default to `postgres` and no password required.

To build an image from the Dockerfile:
>docker build -t demo-postgres .

Where `demo-postgres` is the name you wish to give this image. Then to run the build:
>docker run -p 5432:5432 -d demo-postgres

Remember to expose the ports and use any desired flags.

### Connecting to a Docker PostgreSQL database with `psql`
With your Docker postgres image built and a container running, use `docker exec` to run the `psql` tool on the running container:
>docker exec -it demo-postgres psql -U hello-postgres

Enter your Postgres username after `-U` (`postgres` by default if no `POSTGRES_USER` was set) and enter your password when prompted.

# JDBC API
Java Database Connectivity (JDBC) is an API for connecting to a RDBMS such as Oracle, PostgreSQL, or MySQL. As a collection of classes and interfaces it requires a driver from the database vendor on the classpath. Once added, a `java.sql.DriverManager` will register the driver and act as a factory for a `java.sql.Connection`, used to create and send SQL queries with `java.sql.Statement`, `java.sql.PreparedStatement`, or `java.sql.CallableStatement` objects, and retrieve result sets in `java.sql.ResultSet` objects.

You can load a JDBC driver using `Class.forName()` or `DriverManager.registerDriver()`, or let DriverManager automatically detect the driver on the classpath.

```java
// Loading the driver may not be necessary, but it's good to specify
try {
    Class.forName("org.postgresql.Driver");
} catch (java.lang.ClassNotFoundException e) {
    System.out.println(e.getMessage());
}

// Pay attention to the url pattern
String url = "jdbc:postgresql://host:port/database";
String username = "databaseuser"
String password = "password"

try (
    // Be sure to close all connections after use
    Connection connection = DriverManager.getConnection(url, username, password);
    Statement statement = connection.createStatement();
){
    // executeUpdate() returns the number of rows affected for DML
    int rowCount = statement.executeUpdate("insert into pizza values (1, 'cheese')");

    // executeQuery() returns a ResultSet object for queries
    ResultSet pizzas = statement.executeQuery("select * from pizza");

    // Loop through ResultSet for each row returned
    while(pizzas.next()) {
        System.out.println(pizzas.getInt("id"));
        System.out.println(pizzas.getString("flavor"));
    }

} catch (SQLException ex) {
    
} 
```

## Statement
A Statement object sends queries and updates, as well as receive errors or ResultSets.

**Statement** is prone to SQL Injection attacks, especially if you use a raw string to write the query.

**PreparedStatement** is a precompiled SQL statement. It is best used for writing several similar queries in a loop, but will also as a side effect protect against SQL Injections
```java
PreparedStatement ps = myConnection.prepareStatement("UPDATE ANIMALS SET name=? WHERE id=?");
ps.setString(1, "Hippo");
ps.setInt(2, 7);
ps.executeQuery();
```
**CallableStatement** execute stored procedures and can return 1 or many ResultSets.
```java
CallableStatement cs = myConnection.prepareCall("{CALL BIRTHDAY_SP(?, ?)}");
cs.setInt(1, aid);
cs.setInt(2, yta);
cs.execute();
```

# Transaction Management
The connection objecct will automatically commit every statement to the database, which may not be ideal for batch insertions. To open a transaction, call `connection.setAutocommit(false)` and end the transaction afterwards with `connection.commit()`, then set `connection.setAutocommit(true)` if needed. Use the `rollback()` method if exceptions are thrown during the transaction.


## Resources
### Articles
- [The SQL Standard](https://blog.ansi.org/2018/10/sql-standard-iso-iec-9075-2016-ansi-x3-135/)
- [Life of a SQL query](https://numeracy.co/blog/life-of-a-sql-query)
- [How does a relational database execute SQL statements and prepared statements](https://vladmihalcea.com/relational-database-sql-prepared-statements/)
- [A beginner’s guide to database table relationships](https://vladmihalcea.com/database-table-relationships/)
- [A beginner’s guide to ACID and database transactions](https://vladmihalcea.com/a-beginners-guide-to-acid-and-database-transactions/)
- [A Simple Guide to Five Normal Forms](http://www.bkent.net/Doc/simple5.htm)
- [Say NO to Venn Diagrams When Explaining JOINs](https://blog.jooq.org/2016/07/05/say-no-to-venn-diagrams-when-explaining-joins/)
- [A beginner’s guide to SQL injection and how you should prevent it](https://vladmihalcea.com/a-beginners-guide-to-sql-injection-and-how-you-should-prevent-it/)
- [The anatomy of Connection Pooling](https://vladmihalcea.com/the-anatomy-of-connection-pooling/)

### Books
- [Wikibooks - SQL](https://en.wikibooks.org/wiki/Structured_Query_Language)
- [Wikibooks - PostgreSQL](https://en.wikibooks.org/wiki/PostgreSQL)
- [Wikibooks - Relational Database Design](https://en.wikibooks.org/wiki/Relational_Database_Design)
- [The Internals of PostgreSQL](http://www.interdb.jp/pg/)
- [Database Design](https://opentextbc.ca/dbdesign01/)

### Documentation
- [SQL92 Specification](http://www.contrib.andrew.cmu.edu/~shadow/sql/sql1992.txt)
- [PostgreSQL 12 Documentation](https://www.postgresql.org/docs/12/index.html)
- [PostgreSQL SQL Command Reference](https://www.postgresql.org/docs/12/sql-commands.html)
- [psql](https://www.postgresql.org/docs/12/app-psql.html)
- [PostgreSQL on Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html)
- [Java JDBC API](https://docs.oracle.com/javase/8/docs/technotes/guides/jdbc/)
- [java.sql (JavaSE 8)](https://docs.oracle.com/javase/8/docs/api/java/sql/package-summary.html)

### Tutorials
- [Example of a Step by Step Normalization](https://en.wikipedia.org/wiki/Database_normalization#Example_of_a_step_by_step_normalization)
- [Description of the Database Normalization Basics](https://docs.microsoft.com/en-us/office/troubleshoot/access/database-normalization-description)
- [3 Normal Forms Database Tutorial](http://phlonx.com/resources/nf3/)
- [SQL Bolt](https://sqlbolt.com/)
- [SQLZOO](https://sqlzoo.net/wiki/SQL_Tutorial)
- [postgresql.org Tutorial](https://www.postgresql.org/docs/12/tutorial.html)
- [Postgres Guide](http://www.postgresguide.com/)
- [PostgreSQL Exercises](https://pgexercises.com/)
- [Developer's Guide to PostgreSQL on Linux: psql shell](https://thecodinginterface.com/blog/postgresql-psql-shell/)
- [Setting Up for Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_SettingUp.html)
- [Creating Postgres RDS and Connecting Using pgAdmin](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_GettingStarted.CreatingConnecting.PostgreSQL.html)
- [Oracle Java Tutorials - JDBC Introduction](https://docs.oracle.com/javase/tutorial/jdbc/overview/index.html)
- [Oracle Java Tutorials - JDBC Basics](https://docs.oracle.com/javase/tutorial/jdbc/basics/index.html)
- [JDBC Diver Connection URL strings](https://vladmihalcea.com/jdbc-driver-connection-url-strings/)
- [JDBC Driver Maven dependency list](https://vladmihalcea.com/jdbc-driver-maven-dependency/)
