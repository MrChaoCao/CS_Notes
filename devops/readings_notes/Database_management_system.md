# Database Management System DBMS
System software for creating and managing databases. The DBMS gives users and programmers a systematic way to create, retrieve, update, and manage data.

DBMS is an interface between the database and the end user or application programs.
It ensures that data is consistently organized and remains easily accessible.

DBMS manages 3 things:
1. The data
2. Database engine
  + what allows the db to be accessed, locked, modified
3. The database schema
  + defines database structure

  provides concurencey, security, data integrity and uniform administration procedures

### Typically DBMS tasks are
  * change Management
  * performance monitoring/tuning
  * backup and recovery
  * automatic rollbacks
  * restarts and recovery
  * activity logging and auditing

DBMS provides a centralized view of data
can accessed by multiple users
can accessed from multiple locations
Limits what data the end user sees
Limits how the user can view the data
  + many views of the same schema
End user does not need to know where the data is or how it's stored.

### Types of DBMS
* relational DBMS (RDBMS) have a SQL API.
* NoSQL DBMS best for loosely defined data structures that might change
* In-memory DBMS (IMDBMS) faster response time, better performance
* Columnar DBMS (CDBMS) good for data warehouses with lots of similar data items
* Cloud based DBMS

### Advantages of a DBMS
allows users and programmers to use the same data while maintaining data integrity 
data is better protected and maintained than when a new iteration of the data is reated for every new application
central store of data
