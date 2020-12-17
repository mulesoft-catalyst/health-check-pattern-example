# Health Check Pattern Example

This example provides a basic implementation of the Health Check API pattern. The Health Check API Pattern allows an 
external monitoring tool to continuously track the availability of an API and its dependent systems. This example 
implementation demonstrates:

  - How to define a new resource `/health` the allows external consumers to check the status of an API and its dependent system.
  - How to capture the average response time of the dependent system utilized by the API. 
  - How to capture the average payload size constructed by the API. 

### Why?
In many instances, APIs are built to provide a façade layer for the underlying system. When an API fails, it is rarely 
a failure of the API itself but the underlying system. Thus, it is important to periodically check the health of the 
of the core system to ensure that it is capable of supporting incoming requests. The Health Check API resource 
can perform a variety of system checks to measure availability and performance.


### How?
An external monitoring tool (like Anypoint’s API Functional Monitoring) can periodically invoke the health check operation 
to check the status of the API and its dependent systems. If any errors are uncovered by the operation’s response, the 
monitoring tool can be configured to notify the operations team.

