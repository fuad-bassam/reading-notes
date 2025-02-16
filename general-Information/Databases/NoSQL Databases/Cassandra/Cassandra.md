# Cassandra 
a wild-column database


## Get start 

### Cassandra with Docker container 

```bash
// we create the network because the server communicated with the client with the same network
1. docker network create cassandra_network

2. docker run --name cassandra_server --network cassandra_network -d cassandra 

//Create a client for the cassandra_server so that we can communicate with it  
//-it  means that we run it in "an iterative mode" so we can use it in the console

3. docker run -it --network cassandra_network --rm cassandra cqlsh cassandra_server

OR 
// without create a client do it direct from the server 
3. docker exec -it cassandra_server cqlsh

// test result
4. show version
```

or for simple one we can use this 

```bash 
     1. docker run --name cassandra-container -d -p 9042:9042 cassandra:latest
 
     2. docker exec -it cassandra-container cqlsh
```



### CQL Commands

1. find all created keyspace
    ```cqlsh
    DESCRIBE KEYSPACE;
    ```
2. find all tables inside a keyspace

    ```cqlsh
    DESCRIBE TABLES KEYSPACE_Name;
    ```

## Reference  

[**cassandra Started  Official document**](https://cassandra.apache.org/_/quickstart.html)     


[**Setup Apache Cassandra on Windows using Docker (Server + Client) (video)**](https://www.youtube.com/watch?v=jKp21r59WYg)     


[**Started with ASP NET WebApi part 1 (video)**](https://www.youtube.com/watch?v=CwsimG5edaA)


[**Started with ASP NET WebApi part 2 (video)**](https://www.youtube.com/watch?v=GlDERX0B5HY)


