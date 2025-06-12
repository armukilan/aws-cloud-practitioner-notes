# Database

- Database is a data store that stores semi-structured and structured data
- Database stores more complex data stores because it requires using formal design and modeling techniques

- Databases can generally be categorized as either being: 
	- Relational so structured data that strongly represents tabular data so we're talking about tables rows and columns so there's a concept of row oriented or column oriented 
	- Non relational databases so these are semi-structured that may or may not resemble tabular data

- Functionality of the databases 
	- Special specialized language to query so retrieve data so in this case SQL 
	- Specialized modeling strategies to optimize retrieval for different use cases 
	- More fine-tune control over the transformation of the data into useful data structures or reports 

- Normally a database infers someone is usually using a a relational row oriented data store

## Key-Value store

- Key value database is a type of non-relational database or nosql that uses a simple key Value method to store data.
- Key value stores are dumb and fast uh but they generally lack features like relationships indexes aggregation 
- A key value stores literally a unique key alongside a value
- A key value store interprets this data resebling a dictionary (aka associative array or hash)
- A key Value Store it looks like a tabular data, it doesn't have to have consistant columns per row (so schemaless)
- Due to design, they can scale well beyond a relational DB

## Document stores 

- document store is a nosql database that stores documents as its primary data structure
- A document could be an XML but more commonly is Json or Json like document stores are subclasses of key value stores
- Components of Document store compared to Relational DB

[Database](db1.png)

## AWS DynamoDB

- Dynamo DB is a serverless nosql key value and document database.
- It is designed to scale to billions of records with guaranteed consistent data returned in at least a second. 
- You do not have to worry about managing shards. 

- Dynamo DB is AWS Flagship database service meaning whenever we think of a database service that just scales is cost effective and very fast we should think of Dynamo DB 

- In 2019 Amazon the online shopping retail shut down their last Oracle database and completed their migration to Dynamo DB so they had 7,500 Oracle databases with 75 petabytes of data and with Dynamo DB they reduce that cost by 60% and reduced the latency by 40%  

- Note: When we want a massively scalable database


## DocumentDB 

- A noSQL document database that is "mongoDB DB compatible" 
- Mongodb is very popular noSQL among developers there were open source licensing issues around using open-source mongodb, so AWS got around it by just building their own mongodb database 
- Basically so when you want a MongoDB like database you're going to be using documentDB 

## Amazon Keyspaces 

- This is a fully managed apoe Cassandra database 
- Cassandra is an open source noSQL key value database similar to DynamoDB that is column or store database but has some additional functionality
- When you want to use Apache Cassandra you're using Amazon keyspaces.

# Relational DB

## Relational Database Service

- Relational database service RDS is a relational database service that supports multiple SQL engines 
- Relational is synomous with SQL and online transactional processing (oltp) 
- Relational databases are the most commonly used type of database among tech companies and startups.

- RDS supports the following SQL engines:
	- MySQL this is the most popular open source SQL database and it was purchased and is now owned by Oracle.
	- Mario DB When oracle bought MySql. MariaDB made a fork(copy) of MySQL was made under a different open-source license
	- Postgres (psql) most popular open source SQL database among developers. Has many Rich features over mySQL but but it does come with added complexity 
	- Oracle has its own SQL proprietary database which is well used by Enterprise companies. But you have to buy a license to use it 
	- Microsoft SQL Microsoft's proprietary SQL database and with this one you have to buy a license to use it 
	- Aurora so this is a fully managed database

## Aurora

- Fully managed database of either mysql (five times faster) or posgresQL (three times faster) database 
- when you want a highly available, durable and scalable and secure relational database for postgresql or mysql you want to use Aurora 

## Aurora serverless 

- Serverless on demand version of Aurora 
- When you want the most of the benefits of Aurora but you can trade to have cold starts or you don't have lots of traffic or demand.

## RDS on VMware 

- this allows you to deploy RDS supported engines to on premise data centers 
- the data center must be using VMware for Server virtualization 
- when you want databases managed by RDS on your own dataCenter 


# Other Database Service

## AWS Redshift

- Redshift is a petabyte size data warehouse 
- Data warehouses are for online analytical processing (olap) 
- data warehouses can be expensive because they are keeping data hot - they can run a very complex query and a large amount of data and get that data back very fast 
- when you need to quickly generate analytics or reports from a large amount of data you're going to be using red shift 

## Elasticache 

- Managed database of an in-memory and caching open source databases such as reddis or memcached 
- when you need to improve the performance of an application by adding a caching layer in front of your web servers or database you're going to be using elastic cache 

## AWS Neptune 

- Managed graph database 
- The data is represented as interconnected nodes (I believe that it uses gremlin is the way to interface with it)
- When you need to understand the connections between data eg. mapping fraud Rings or social media relationships 
- very relational database heavy information you're going to want to use Neptune 

## Amazon time streams 

- Fully managed time series database 
- Think of devices that send lots of data that are time-sensitive such as iot devices 
- when you need to measure how things change over time 

## Amazon Quantum Ledger database 

- this is a fully managed Ledger database that provides transparent immutable cryptographically variable transaction logs 
- when you need to record a history of financial activities that can be trusted 

## Database migration service (DMS) 

- It's not a database but it's a migration service so you can migrate from 
	- on premise database to AWS 
	- from two databases in different or same AWS accounts using different SQL engines 
	- from an SQL to a nosql database 
