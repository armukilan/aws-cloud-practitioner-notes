# Application Integration

- application integration is the process of letting independent applications to Communicate and work with each other commonly facilitated by an intermediate system 
- Cloud workloads strongly encourage systems and services to be Loosely coupled and so AWS has many services for the specific purpose of application integration 

- The common systems or design patterns that utilize application integration 
	- queuing 
	- streaming 
	- Pub sub 
	- API gateways 
	- State machines 
	- event buses and 

- There are more but that's what I could think about that are the most common ones

# Queuing and SQS

- Messaging System- Used to provide asynchronous communication and decouple processes via messages and events from a sender and receiver (producer and a consumer)

## Queing system 

- messaging system that generally will delete messages once they are consumed. 
	- it's for simple communication 
	- it's not real time 
	- you have to pull the data 
	- it's not reactive 
- a good analogy would be imagine people that are queuing in a line to go do something 


## AWS Simple queuing service (sqs) 

- it's a fully managed queuing service that enables you to decouple and scale microservices, distributed systems and serverless applications 
- very common use case in a web application would be to queue up transactional emails to be sent like sign up, reset password 

- the reason why we have queuing to decouple those kind of actions is that if you had a long running task and you had too many of them it could hang your applications so by decoupling them and letting a separate compute service take care of that would be something that would be very useful. 

# Streaming and Kinesis
 
- you have multiple consumers that can react to events (messages) ( in a queing system we just call them messages)
- events live in the Stream for long periods of time so complex operations can be applied 
- generally streaming is used for Real Time stuff whereas queuing is not necessarily real time 

## Amazon Kinesis

- you could also use Kafka 
- Amazon Kinesis is the AWS fully managed solution for collecting processing and analyzing streaming data in the cloud 
- so the idea is that you have these producers so that are producing events could be ec2 instances mobile devices could be a computer or traditional server they're going to go into the data stream there's a bunch of shards that scale and there's consumers on the other side so maybe red shift wants that data Dynamo DB S3 or EMR okay but the thing you have to remember is that streaming Is For Real Time data and as you can imagine because it's real time and it's doing a lot more work than um a queuing system

[Kinesis](kinesis.png)

# Pub/Sub

- pub/sub so this stands for publish subscribe pattern commonly implemented in messaging systems 
- In a pub sub system the sender of messages (the Publishers) do not send their message directly to receivers 
- they instead send their messages to an event bus 
- the event bus categorizes their messages into groups 
- then receivers of messages (subscribers) subscribe to these groups
- whenever new messages appear within their subscriptions the messages are immediately delivered to them 

[PubSub](pubsub.png)

- the publisher has no knowledge of who the subscribers are 
- subscribers do not pull for messages 
- messages are instead automatically and immediately pushed to the subscribers 
- messages and events are interchangeable terms in Pub sub

- Eg. A real-time chat system, A web hook system

## AWS Simple Notification Service

- SNS is a highly available, durable, secure, fully managed, Pub sub messaging service that enables you to decouple micro-services, distributed systems and serverless applications.

[SNS](sns.png)

# API Gateway

- API Gateway is a program that sits between a single entry point and multiple backends
- API Gateway allows for throttling, logging, routing logic or formatting of the requests and response

## Amazon API Gateway

- Solution for creating secure API in your Cloud environment at any scale create 
- Create API that act as a front door for applications to Access Data, Business logic or functionality from backend services.

[API gateway](apig.png)

# State Machine

- State machine is an abstract model which decides how one state moves to another based on a series of conditions 
- Think of a state machine like a flowchart and for AWS the solution here is AWS Step function 

## AWS Step Function

- Coordinate multiple AWS Services into a serverless workflow 
- a graphical console to visualize the components of your application as a series of steps 
- automatically trigger and track each step and retries when there are errors so your application executes in order as expected every time 
- logs the state of each step so when things go wrong you can diagnose and debug problems quickly

# Event Bus

- an event bus receives events from a source and routes events to a Target based on rules 

[Event Bus](evebus.png)

- Eg. We have an event it enters the event bus we have a rules tell it to go to the Target it's that simple and we have been seeing event buses in other things like streaming and Pub sub but AWS has this kind of event bus offering that is kind of high level it's called event bridge 

## AWS EventBridge

- It's a service event bus service that is used for application integration by streaming realtime data to your applications 
- the service was formerly known as Amazon cloudwatch events they give it a renaming to give it a better opportunity for users to know that it's there to use

[Eventbridge](eb.png)

# Highlights of all the services

[All services](overall.png)

