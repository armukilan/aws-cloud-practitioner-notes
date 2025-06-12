# Data Warehouse

- Data warehouse is a relational data store designed for analytical workloads which is generally column oriented data 
- Companies will have terabytes and millions of rows of data and they need a fast way to be able to produce analytics reports 

- Data warehouses generally perform aggregation 
	- aggregation is the idea of grouping data together so find a total or an average 
	- data warehouses are optimized around columns since they need to quickly aggregate column data

- Data warehouses are generally designed to be hot 
	- Hot means that they can return queries very fast even though they have vast amounts of data 

- Data warehouses are infrequently accessed meaning they aren't intended for real-time reporting but maybe once or twice a day or once a week to generate business and user reports 

- A data warehouse needs to consume data from a relational database on a regular basis and again it can consume it from other places but you'll have to transform it to get it in there 