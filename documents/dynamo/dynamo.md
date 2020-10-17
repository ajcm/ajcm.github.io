# AWS DynamoDB

DynamoDB is a NoSql database that supports key-value and document data structures.

### Primary Key
The primary key must be unique.

**Partition key**
Single unique value from one of the attributes, this is also known as the *HashKey*

**Composite Key**
Combination of two values, the partition key plus a *Range* or *Sort Key* that can be used to order the values. In a composite key the hash key can be the same for multiple values but the combination must be an unique value.

### Operations

#### Put, Get, Delete
This methods use the primary key to insert and retrieve values.

#### Query
Run a query through the values of the key or an index.

**KeyConditionExpression**
This a mandatory field, the Key condition expression can only contain the attributes that correspond to the key, two at most in the case of a composite key.

Expression:
Partition Key - equal/not equal
Sort Key - equal/not equal/ less than/greater than

If the sort key corresponds to a attribute from a numeric data type the values are returned by the order of that attribute

**FilterExpression**
The filter expression can have values that don't belong to the key, this selection occurs after the values are retrieved.
Contrary to the KeyExpression this as no impact in the processing cost of query operation.


#### Scan
Retrieves all items from the table, the operation can be more expensive than a query so that the last is preferred.

**FilterExpression**
Filter expression can have any field.


### Index
By default queries are tangled to the primary key, the way one can use other attributes in the query is to use an Index, there are two types:

**Local Secondary Index (LSI)**
If one want to run a query using the same partition key but a different sort key a LSI can be specified at table creation table.

**Global Secondary Index**
To use query a different partition key a GSI must be created (can be after table creation), however this index comes at a cost because it requires provisioned throughput.


### Structure

Document

|scope| id |  

| id | section | 

[Javascript Client](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/DynamoDB/DocumentClient.html)

