## Netflix stack solves

* **Eureka, Hystrix, Feign and Ribbon** manages connection between services
* **Ribbon** retries requests when failure occurs
* **Ribbon** load balance traffic to the right place
* **Hystrix** prevent failure cascading (usually implementing circuit breaker pattern)
* **Hystrix** monitor traffic between services
* **Sleuth** trace request with correlation ids
* You have to secure connection (TLS) yourself