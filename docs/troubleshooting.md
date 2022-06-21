## Intro
The Throubleshooting interview it's something "weird" that not all the companies do and it's something hard to prepare.  
But preparing for system design could help you.

Usually it's an open ended question such as:  

!!! example ""
    two hours ago, we started getting alerts that ~5% of our customers cannot see ads

Starting from there, you have to ask questions to retrieve more info, as if we were playing D&D.  
The goal here is to understand how you tackle problems and your reasoning process to get to the solution (but usually it is not mandatory to reach the end).


## Advices
As we said, we should ask clarifying questions  
Imagine you are in a real situation and just explain what you would do, where would you search for clues, what would you look for, etc...

The important thing is to show good thinking, good analytical skills, general knowledge of how different software systems work, and that you know how to deal with problems and try to solve them.


## Topics
Preparing for [System Design](../system-design) will help you with the Troubleshooting interview.  
So be prepared to talk about things like:

 - Accessing Servers
 - Viewing Logs
 - Tracing and Metrics
 - Unix Commands
 - Distributed Systems


#### Example Questions

!!! question "Examples"
    - is it a distributed system? Do we have multiple regions?
    - What’s the infrastructure? (k8s?)
    - What Does the system look like? (services, dependencies, dbs, etc)
    - have we released a new version recently?
    - do we have __logs__ and are they searchable?
    - can we look at fields of alerting metrics?
    - does it affect all clients or a specific one? (mobile, desktop, etc)
    - is the problem global or a small area? (maybe it’s only one region or zone)
    - maybe it’s just one replica?
    - service/kernel/system version? Is it the same for every replica?
    - Do we have tracing? -> easier to form hypothesis
    - Do we know which host and timestamp to look at?


## Resources
- [UNIX and Linux System Administration Handbook](https://www.goodreads.com/book/show/8772005-unix-and-linux-system-administration-handbook)