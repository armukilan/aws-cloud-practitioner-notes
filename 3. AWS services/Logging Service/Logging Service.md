# Logging Service

[Introduction](log1.png)

## AWS CloudTrial

- Service that enables governance, compliance, operational auditing, and risk auditing of your AWS account.

- AWS cloud trail is used to monitor API calls and actions made on AWS account 
- easily identify which users and accounts made the call to AWS 
	- WHERE so the source IP address 
	- when the eventtime 
	- who the user, useragent 
	- what the region, resource and action 


## AWS Cloud trail 

- Already logging by default and will collect logs for the uh for the last 90 days via event history.

- if you need more than 90 days you need to create a trail which is very common you'll go into AWS and make one right away 
- trails are outputed to S3 and do not have like event history to analyze a trail. you have to use Amazon Athena or other tools

## Cloudwatch Alarm

[Cloudwatch Alarm](log2.png)

[Anatomy of Alarm](log3.png)

[Log Streams](log4.png)

[Log Events](log5.png)

[Log Insights](log6.png)

[Log insights](log7.png)

[Log insights](log8.png)