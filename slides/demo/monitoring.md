## Monitor all the things

Cleanup kubernetes cluster :

```bash
./resiliency-cleanup.sh
./poc-istio-rules.sh
```

Run JMeter thread group *Retrieve PSU authentication information* 

* Monitor Kubernetes cluster using Heapster ```http://CLUSTER_IP:30002```
* Monitor the request traces and latency using Zipkin ```http://CLUSTER_IP:30411```
* Monitor the Istio service mesh using Prometheus and Grafana : ```http://CLUSTER_IP:30300```