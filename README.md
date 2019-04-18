# RSS Feed Aggregator

## Authors

- Nishtha Shrivastav (2594-5398)
- Pulkit Tripathi (9751-9461)
- Akash Shingte (4874-1966)

## Contributions

- Nishtha Shrivatav
    - Developed the logic for parsing OPML Files parallely.
    - Developed the Thread pool implementation.
    - Developed the Direct Mapping implementation.
    - Tests for Thread pool with different thread sizes.

- Pulkit Tripathi
    - Set up the framework of the Spring project.
    - Callable FeedParser implementation
    - SimpleFeedAggregator (aggregation using threadpool without blocking queues and direct mapping) implementation
    - Tests for correctness of aggregation.
    - Complete Angular front end for displaying feeds.
    - Architecture design 

- Akash Shingte
    - Implementation of BlockingQueueFeedAggregator and FeedScanner.
    - Tests for the Blocking Queue implementation of aggregation
    - Refactored FeedMessage with comparator.
    - Execution speed tests.
    - Architecture design

## Project Description

RSS Feed aggregator is the perfect project to show how the power of multithreading. It is a means to show the famous problem of producer-consumer. There are multiple RSS Feed available on the web.To get their content of various in one place we need to -
Request for that web page
1. Wait till we receive a response of the feed
2. Parse the elements of the feed
3. Aggregate the result of various sources

Doing these 4 tasks in serial manner will take a long time and doesn’t utilize the computing power we have.If we delegated the tasks to multiple processors to do these process in a concurrent manner we will achieve faster retrieval of information.

In this project, we used various techniques to delegate tasks for creating concurrent execution tasks. The various techniques we tried are -

- Blocking queues
- Thread Pools
- Direct Mapping to Threads


## Pre-requisite for building

1. Spring Boot
2. Node
3. Node package manager
4. Maven
5. Angular CLI

### Spring boot

<Add instructions to install spring boot>

### Node package manager

<Add instruction to install npm>

### Maven

<Maven to build the spring project>
<Instruction to get maven>

### Angular CLI

<Instruction to get Angular CLI>

## Build the project

`mvn compile`

## Executing the project

`mvn package`

## To start application:

### Using maven

`mvn spring-boot:run`

### Using jar file:

`java -jar .\target\rss-aggregator-0.0.1-SNAPSHOT.jar`

### Angular JS application

`cd webui`
`ng serve --open`
