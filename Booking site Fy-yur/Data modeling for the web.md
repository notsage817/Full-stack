
#### Methods for sending data to flask
+ XMLhttprequest
+ fetch
### TCP/IP
TCP/IP is a suite of communication protocols that is used to connect devices and transfer data over the internet.
+ IP addresses:Identify the location of a computer on a network
+ Ports: Location on the recipient computer
+ Port number: specify where on the computer a particular connection should be made
  + port 80:commonly used for HTTP requests
  + port 5432:used by most database systems, default for Postgres

TCP/IP is **connection-based**, a connection is established before any data transmission begins
+ Deliveries over the connection are error-checked
+ A session starts when connecting, many transactions occur during a session
(UDP stands for User Datagram Protocol on which hosts send data without any connections needing to be established)
>If TCP is like building highways between houses before sending packages between them, then UDP is much like sending over a carrier pigeon from one house to another in order to deliver packages: you don't know whether the pigeon will head in the right way, drop your package along the way, or encounter an issue mid-travel. On the other hand, there is less overhead to use UDP than managing a connection over TCP / building a highway.
>
>When speed is more important than reliability, especially when applications need to stream very small amounts of information quickly (smaller packages of information means less issues with reliability), then UDP is preferred. A lot of real time streaming applications, (e.g. live TV streaming, Voice over IP (VoIP)) prefer UDP over TCP. Since UDP does not need to retransmit lost datagrams, nor does it do any connection setup, there are fewer delays over UDP than TCP. TCP's continuous connection is more reliable but has more latency.

Work is bundled into transactions, transactions commit work to the database.
Databases are interacted using client-server interactions, like Postgres using TCP/IP to be interacted with.
>In case of system failures, data in your database is still kept in a valid state (by rolling back the entire transaction if any part of it fails). To ensure a database is consistent before and after work is done to it, databases uses atomic transactions, and actions like commits and rollbacks to handle failures appropriately. Transactions are, in other words, ACID.


### DBAPI
A tool that is used to interact with database and use its results in a specific programming language.
+ Provides a standard interface for one programming language to talk to a relational database server
+ Low level library for writing SQL statements that connect to a database
+ Known as database adapters

### SQLAlchemy
The most popular open-source library for working with relational databases from python, aka Object-Relational Mapping library that provides an interface for using object oriented programming to interact with database.

**SQLAlchemy generates SQL statements and DBAPI sends them to the database**
![image](https://user-images.githubusercontent.com/59595363/145167615-82120a89-c650-46a3-bbf2-bc46dc0b0aaf.png)
+ Dialect is used to communicate with various types of DBAPI implementations and databases.
+ A connection pool is a standard technique used to maintain long running connections in memory for efficient re-use, as well as to provide management for the total number of connections an application might use simultaneously.
