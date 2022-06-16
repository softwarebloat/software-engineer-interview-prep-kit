# Glossary
Here you can find some key arguments of computer science that usually could be asked in interviews

!!! warning
    This list is intended as a starting point to brush up on some topics and not as a complete resource that cover every aspect of a specific topic.  
    If you do not know any of the topics presented, please read more elsewhere.

## API Gateway
separate business logic from common operations like:  
Authentication, Authorization, DDoS protection, routing, serve static response, caching responses, load balancing, A/B testing


## Authentication vs Authorization
In simple terms, authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to.

## Automation (CI/CD) TODO

## Availability
Is the time a system remains operational to perform its required function in a specific period.


## Bloom Filter
A __Bloom filter__ is a data structure designed to tell you, rapidly and memory-efficiently, whether an element is present in a set.  
The price paid for this efficiency is that a Bloom filter is a probabilistic data structure: it tells us that the element either definitely is not in the set or may be in the set.


## CAP Theorem
CAP stands for: _Consistency_, _Availability_, _Partition tolerance_  
This theorem states that any distributed system can only achieve 2 of these 3 properties.  

!!! info
    since almost all useful systems do have _network-partition tolerance_, it’s generally boiled down to __Consistency VS Availability__.

## CDN
Stands for __Content Delivery Network__ (CDN) refers to a geographically distributed group of servers which work together to provide fast delivery of Internet content.  

__Benefits__: 

- Improving website load times 
- Reducing bandwidth costs 
- Increasing content availability and redundancy 
- Improving website security(DDoS mitigation)

## Cache
Caching is the mechanism of storing data in a temporary storage location, usually in memory, so that requests to the data can be served faster.

Caching improves performance by decreasing page load times, and reduces the load on servers and databases.  
__Cache hit__: return response without ask data to server or db  
__Cache miss__: request sent to the server or db to fetch result. Result is than cached to the temporary storage and returned to the client

### Cache invalidation methods
When data is updated in the database, then that data has to be refreshed in the cache as well. This is called cache invalidation.

| Method                            | Description                                                 |
| --------------------------------- | ----------------------------------------------------------- |
| `Write-through cache`             | Data is written to the cache and database at the same time. |
| `Write-around cache`              | Data is written to the database writing to cache. Data is written to cache when a request results in a 'cache miss', at which point data is retrieved from the database, written to cache, and sent back to the client. |
| `Write-back (Write-behind) cache` | Data is written to the cache without writing to the database. Data is written to the database asynchronously. |

### Eviction algorithms
First In First Out (__FIFO__)
Last In First Out (__LIFO__)
Least Recently Used (__LRU__)
Least Frequently Used (__LFU__)
Least Frequent Recently Used (__LFRU__)


## Consistent Hashing
Is a hashing technique such that when a hash table (key map to the machine) is resized, only n/m keys need to be remapped.  

| Key | Description     |
| --- | --------------- |
| N   | number of keys  |
| M   | number of slots |


## DNS
The __Domain Name System__ (DNS) is the phonebook of the Internet that maps domain names to IP addresses.

## Database (TODO)
Which use? (SQL vs NoSQL)  
Scaling (vertical vs horizontal/sharding)

### Sharding:
Is the act of splitting a db into 2 or more pieces called shards.  
Popular sharding strategies:  

- based on client’s regions
- based on the type of data stored (user data in one shard; payments data stored in another)
- based on the hash of a column (only for structured data)

### DB Replication
Backup  
Vertical Scaling VS Horizontal Scaling


## DoS
Is typically accomplished by flooding the targeted machine or resource with superfluous requests in an attempt to overload systems

## Eventual Consistency
> A consistency model which is unlike Strong Consistency.

In this model, reads might return a view of the system that is stale.
An eventually consistent datastore will give guarantees that the state of the database will eventually reflect writes within a time period (seconds or minutes)


## Gossip protocol
Is a communication protocol that allows state sharing in distributed systems.  
he protocol enables each node to keep track of state information about the other nodes in the cluster, such as which nodes are reachable


## HTTP
__HTTP__ (Hypertext Transfer Protocol) is an (application layer) protocol designed to transfer information between networked devices.  
A typical flow over HTTP involves a client machine making a request to a server, which then sends a response message.


## HTTP Error Codes

| Error Code | Description
| ---------- | --------------------------------------- |
| __1xx__        | indicates an informational message only |
| __2xx__        | indicates success of some kind          |
| __3xx__        | redirects the client to another URL     |
| __4xx__        | indicates an error on the client’s part |
| __5xx__        | indicates an error on the server’s part |

## HTTP Methods
| Method     | Description                                                                                                 |
| ---------- | ----------------------------------------------------------------------------------------------------------- |
| `GET`      | requests a representation of the specified resource. Requests using GET should only retrieve data.          |
| `HEAD`     | asks for a response identical to a GET request, but without the response body.                              |
| `POST`     | submits an entity to the specified resource, often causing a change in state or side effects on the server. |
| `PUT`      | submits an entity to the specified resource, often causing a change in state or side effects on the server. |
| `DELETE`   | deletes the specified resource.                                                                             |
| `CONNECT`  | establishes a tunnel to the server identified by the target resource.                                       |
| `OPTIONS`  | describes the communication options for the target resource.                                                |
| `TRACE`    | performs a message loop-back test along the path to the target resource.                                    |
| `PATCH`    | applies partial modifications to a resource.                                                                |


## HTTPS
__Hypertext Transfer Protocol Secure__ (HTTPS) is the secure version of HTTP.  
Technically speaking, HTTPS is not a separate protocol from HTTP.  
It is simply using __TLS/SSL__ encryption over the HTTP protocol. 

HTTPS occurs based upon the transmission of TLS/SSL certificates, which verify that a particular provider is who they say they are.

## JWT (TODO)

## LoadBalancer
reduces individual server load and prevents application servers from becoming a single point of failure forwarding traffic only to “health” services.  
It could use different algorithms to do so like Round Robin or load-aware balancers

### Algorithms

| Method                        | Description
| ----------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `Least Connection Method`     | Routes request to the server having the least number of active connections.                                                   |
| `Least Response Time Method`  | Routes request to the server having the least number of active connections and lowest average response time.                |
| `Round Robin Method`          | Routes request to the first available server and then moves it to the end of the queue.                                       |
| `Weighted Round Robin Method` | Routes request to the first available server having the highest weight. Each server is assigned a weight, an integer number, based on its processing capacity. |


## Message queue vs message broker
A __message queue__ is a data structure, or a container - a way to hold messages for eventual consumption.  
A __message broker__ is a separate component that manages queues.  
Brokers: Kafka, RabbitMQ, SNS/SQS


## Monitoring (TODO)

### Logging (TODO)
Levels: Debug -> Info -> Warn -> Error

### Metrics (TODO)

### Tracing
The goal of tracing is to follow a program’s flow and data progression.  
Tracing allows you to see how you got there: which function, the function’s duration, parameters passed, and how deep into the function the user could get.

## Pulling vs streaming (websockets)
### __Short polling__
client continuously makes call to the server to retrieve data  

| :green_circle: Pros             | :red_circle: Cons              |
| ------------------------------- | ------------------------------ |
| you can have a stateless server | tons of requests to the server |


### __Long polling__  
client makes the request to the server.  
The server can respond with the data requested or, if not ready/presents, it will keep open the connection to respond to the client when ready.  

| :green_circle: Pros               | :red_circle: Cons                                 |
| --------------------------------- | ------------------------------------------------- |
| not overload server with requests | you tie up a connection between client and server |


### __Web sockets (TCP)__  
open a connection between client and server and keep it open in both ways

| :green_circle: Pros                                  | :red_circle: Cons                                 |
| ---------------------------------------------------- | ------------------------------------------------- |
| server is in control to when send data to the client | a connections is opened between them the all time |



## REST
__REST__ is an _architectural style_, or design pattern, for APIs.  
REST stands for __REpresentational State Transfer__. It means when a RESTful API is called, the server will transfer to the client a representation of the state of the requested resource.  
A resource can be any object the API can provide information about


## Rate limiting
Is used to control the rate of requests sent or received.  
It can be used to prevent DoS attacks, or limit api usage.


## Redundancy
Consists in a duplication of components of a system that tries to increase the reliability of this system.

## Reliability
Is the probability a system will fail in a given period.
A distributed system is considered reliable if it keeps delivering its services even when one or several of its software or hardware components fail. 

redundancy has a cost to achieve such resilience for services by eliminating every single point of failure.


## SLA - Service-Level Agreement
The agreement you make with your users.  
Typically make guarantees on a system’s availability.

## SLO - Service-Level Objective
The objectives your team must hit to meet that agreement.  
Usually about specific metrics like uptime or response time.


## Scalability
is the capability of a system, process, or a network to grow and manage increased demand.

| Scaling Type                               | Description                          |
| ------------------------------------------ | ------------------------------------ |
| :material-dots-horizontal: `Horizontal`    | :material-server: More machines      |
| :material-dots-vertical: `Vertical`        | :muscle: More power                  |

## Stateful (TODO)
dedicated storage

## Stateless (TODO)
shared storage

## TCP vs UDP
__UDP__ is faster than __TCP__ but less reliable.  
__TCP__ establish connection via “handshake” (SYN -> SYN-ACK -> ACK)  
__TCP__ indicates and confirms the order in which order packets should be received. UDP does not.  

Because of that, UDP is much faster but could lose packets (datagrams).   
So applications that use UDP must be able to tolerate errors (loss and duplication).  

So UDP is commonly used in time-sensitive communication where occasionally dropping packets is better than waiting (like voice and video application or online gaming and DNS servers)


## TLS
__TLS__ uses a technology called public key encryption:  
there are two keys, a public key and a private key, and the public key is shared with client devices via the server's SSL certificate.   

When a client opens a connection with a server, the two devices use the public and private key to agree on new keys (TLS handshake), called session keys, to encrypt further communications between them.


## Thread vs Process
__Processes__ are basically the programs that are dispatched from the ready state and are scheduled in the __CPU__ for execution
A process can create other processes which are known as Child Processes.  
Process is isolated (doesn’t share memory with other process)  

__Thread__ is the segment of a process (a process can have multiple threads)  
Threads are faster and share memory


## pub/sub
Is a messaging model that consists of __publishers__ and __subscribers__.  
Publishers __publish__ messages to topics (also called channels) without knowing who will read those messages.  
Subscribers __subscribe__ to topics and read messages coming through those topics.