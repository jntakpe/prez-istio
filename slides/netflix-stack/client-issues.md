## Issues with Netflix OSS

* Application must be written in Java or JVM language (Kotlin, Groovy, ...)
* Difficult to integrate with other stacks than Spring
* Binary size is important (75Mo for app tpp-management)
* Applications are slow to start
* Hystrix uses a thread blocking model
* Applications consumes a lot of memory
* Infrastructure code is embedded into applications
