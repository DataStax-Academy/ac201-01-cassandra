<div class="top">

# Connecting to Cassandra
### [◂](command:katapod.loadPage?step7){.steps} Step 8 of 8 [▸](command:katapod.loadPage?finish){.steps}
</div>

We use the CQL shell, a command-line client, to connect to Cassandra and execute CQL statements.

Start the CQL shell:
```
cqlsh
```

Create the keyspace, table and row in Cassandra:
```
CREATE KEYSPACE killr_video
WITH replication = {
  'class': 'SimpleStrategy', 
  'replication_factor': 1 };
  
USE killr_video;

CREATE TABLE users (
  email TEXT PRIMARY KEY,
  name TEXT,
  age INT,
  date_joined DATE
);

INSERT INTO users (email, name, age, date_joined) 
VALUES ('joe@datastax.com', 'Joe', 25, '2020-01-01');  
```

Retrieve the row from Cassandra:
```
SELECT * FROM users
WHERE email = 'joe@datastax.com';
```

[continue](command:katapod.loadPage?finish){.orange_bar}
