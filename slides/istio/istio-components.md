## Components

* **Envoy** high performance proxy developed in C++ by Lyft to mediate all inbound and outbound traffic for all services.
 Envoy is deployed as a sidecar.
* **Mixer** is responsible for enforcing access control and usage policies across the service mesh and collecting telemetry data from the 
 Envoy proxy and other services.
* **Pilot** provides service discovery for the Envoy sidecars, traffic management capabilities for intelligent routing 
 (e.g., A/B tests, canary deployments, etc.), and resiliency (timeouts, retries, circuit breakers, etc.). 
 It converts high level routing rules that control traffic behavior into Envoy-specific configurations, and propagates them to the sidecars 
 at runtime.
* **Istio auth** provides strong service-to-service and end-user authentication using mutual TLS, with built-in identity and credential 
 management. It can be used to upgrade unencrypted traffic in the service mesh, and provides operators the ability to enforce policy based 
 on service identity rather than network controls.