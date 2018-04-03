With microservices architecture your app needs to :

* Manage connection between services
* Retry requests when failure occurs
* Load balance traffic to the right place
* Prevent failure cascading (usually implementing circuit breaker pattern)
* Monitor traffic between services
* Trace request with correlation ids
* Secure connection (TLS)
* ...