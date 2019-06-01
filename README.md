# consul-service-discovery-example

Learn to create Microservices, based on Spring cloud, registering on HashiCorp Consul registry server and how other microservices (discovery clients) use it to register and discover services to call their APIs.

We will be using Spring Boot based Spring Cloud API. We will use Consul registry server for building the service registry server and generic discovery clients which will register themselves and discover other services to call REST APIs.

Consul provides multiple features like service discovery, configuration management, health checking and key-value store etc. Today we will concentrate on service registry and discovery part. We will develop the below components to build a distributed Eco system where each component is somehow dependent on each other, yet they are very much loosely coupled and of course fault tolerance.

- Consul Agent – running on localhost acting as discovery/registry server functionality.
- Student Microservice – which will give some functionality based on Student entity. It will be a rest based service and most importantly it will be a discovery service client, which will talk with Consul Server/Agent to register itself in the service registry.
- School Microservice – Same type as of Student service – only added feature is that it will invoke Student service with service look up mechanism. We will not use absolute URL of student service to interact with that service. We will use Consul discovery feature and use that to look up student service instance before invoking that.

Here is the overall component interaction diagram for the same.

![alt text](https://cdn2.howtodoinjava.com/wp-content/uploads/2017/07/Main.jpg)

Tech Stack and Runtime
- Java
- Intellij IDE
- Consul as Service Registry Server
- Spring cloud
- Spring boot
- Spring Rest
- Maven

