## Redis Basics

Redis is an open source (BSD licensed), in-memory data structure store, used as a database, cache, and message broker. Redis provides data structures such as strings, hashes, lists, sets, sorted sets with range queries, bitmaps, hyperloglogs, geospatial indexes, and streams. Redis has built-in replication, Lua scripting, LRU eviction, transactions, and different levels of on-disk persistence, and provides high availability via Redis Sentinel and automatic partitioning with Redis Cluster.

## To start the Redis server

1. redis-server
2. redis-cli

## Notes

{key :"value"} → value is always a string (key value pair)

Numbers ⇒ "10020"

Objects ⇒ {key : "{ a : '1' }" }

Array ⇒ {key : "[1,2,3,4]" }

---

## Basic Commands

1. SET → SET <key> <value>
2. GET → GET <key>
3. DEL → DEL <key>
4. EXISTS → EXISTS <key>
5. KEYS \* → displays all available keys
6. FLUSHALL → Deletes everything
7. TTL → Time to live { TTL <key> }
8. EXPIRE → EXPIRE <key> <duration(in sec)>
9. SETEX → SETEX <key> <seconds> <value>

---

## ARRAY OPERATIONS

1. LPUSH → insert from left side → LPUSH <key> <Elements....>
2. RPUSH → insert from right side → RPUSH <key> <Elements....>
3. LPOP → Delete from left → LPOP <key> <count>
4. RPOP →Delete from right → RPOP <key> <count>
5. LRANGE → Iterating through the array → LRANGE <start index {eg: 0}> <end index {eg : -1}>
6. SADD → Allows only unique String elements in the array ( tip : if you have to insert words with space write it within double quotes else it will take it as 2 words ; by default it takes input as Strings

   { SADD <key> <members ..>

7. SMEMBERS → SMEMBERS <key>

---

## HASHES (kind of objects)

1. HSET → HSET <key> <field i.e. attribute name eg roll , name etc. > <value>
2. HGET → HGET <key> <field>
3. HGETALL → HGET <key>
4. HDEL → HDEL <key> <field>
5. HEXISTS → HEXISTS <key> <field> → returns 0 or 1

## PostgreSQL Commands

> SEMI COLON IS IMPORTANT

## To start the SQL server

1. psql -U postgres -h localhost
2. Enter the password

## Create a new User for Database

1. CREATE USER <user_name> WITH PASSWORD <'password'>

## Create a new User for Database and grant all privilegs

1. CREATE DATABASE <database_name>
2. GRANT ALL PRIVILEGES ON DATABASE <database_name> to <user_name>

## Basic Commands

1.  /l → Lists all Databases
2.  DROP → { DROP DATABASE <database_name> } → Deletes the database
3.  \c → { \c <database_name> } Connect the database

## Table operations

1. CREATE TABLE <table_name> (

- <column_name -1> <Type> <primary key , not null etc> ,

  ID INT NOT NULL ,

  NAME CHAR[50],

  AGE INT,

  ADDRESS TEXT

  );

1. \d → Lists all tables within a database
2. \d <table_name> → description of entire table
