## Clients libraries

* Eureka client used to register a service to Eureka's service discovery server
* Ribbon to route request between different service instances
* Hystrix to ensure request delivery and protect from failure cascading
* Hystrix dashboard client to push metrics to dashboard
* Feign to execute request to services inside a Hystrix thread
* Sleuth to trace request and push them to Zipkin dashboard
