# AWS Well-Architected Framework

[Architecture](waf1.png)

# Amazon Leadership principle

- Set of principles used during problem solving, problem solving, simple brain storming, hiring
	- customer Obsession so instead of worrying about what your competitors are doing think about what the customer wants work your way back and uh you know really focus on the customer's  
	- ownership so if you're going to go do something uh you know try to be your own mini boss and take responsibility for whatever it is you're building 
	- invent and simplify so you know always look for the simplest solution don't try to engineer something super complicated if it's not necessary 
	- or right a lot so you know try to be right 
	- learn and be curious so that's pretty self-explanatory 
	- hire and develop the best 
	- insist on the high standards 
	- think big 
	- bias for Action 
	- frugality
	- earn trust 
	- dive deep 
	- have a backbone disagree and commit 
	- deliver results 
	- strive to be the earth's best employer 
	- success and scale bring broad responsibility

- Refer [Principles](https://www.amazon.jobs/en/principles)


# General design principles

The Well-Architected Framework identifies a set of general design principles to facilitate good design in the cloud:

- Stop guessing your capacity needs: If you make a poor capacity decision when deploying a workload, you might end up sitting on expensive idle resources or dealing with the performance implications of limited capacity. With cloud computing, these problems can go away. You can use as much or as little capacity as you need, and scale in and out automatically.

- Test systems at production scale: In the cloud, you can create a production-scale test environment on demand, complete your testing, and then decommission the resources. Because you only pay for the test environment when it's running, you can simulate your live environment for a fraction of the cost of testing on premises.

- Automate with architectural experimentation in mind: Automation permits you to create and replicate your workloads at low cost and avoid the expense of manual effort. You can track changes to your automation, audit the impact, and revert to previous parameters when necessary.

- Consider evolutionary architectures: In a traditional environment, architectural decisions are often implemented as static, onetime events, with a few major versions of a system during its lifetime. As a business and its context continue to evolve, these initial decisions might hinder the system's ability to deliver changing business requirements. In the cloud, the capability to automate and test on demand lowers the risk of impact from design changes. This permits systems to evolve over time so that businesses can take advantage of innovations as a standard practice.

- Drive architectures using data: In the cloud, you can collect data on how your architectural choices affect the behavior of your workload. This lets you make fact-based decisions on how to improve your workload. Your cloud infrastructure is code, so you can use that data to inform your architecture choices and improvements over time.

- Improve through game days: Test how your architecture and processes perform by regularly scheduling game days to simulate events in production. This will help you understand where improvements can be made and can help develop organizational experience in dealing with events.

Note: Goto whitepaper and read the overview and design principles of each topic.

## First 5 pillars

[OE](waf2.png)

[Security](waf3.png)

[Reliability](waf4.png)

[Performance Efficiency](waf5.png)

[Cost Optimization](waf6.png)

## AWS Well-architected tool

- Auditing tool to be used to asset your cloud workloads for alignment with AWS Well architected framework
- It is a checklist, with nearby references to help you assemble a report to share with executives and key stake-holders

## AWS well-architecture center

- Web portal that contains best practices and reference architectures for a variety of different workloads. View- [Link](https://aws.amazon.com/architecture)