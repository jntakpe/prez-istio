## Control ingress traffic

Initialize configuration :

```bash
./poc-infra.sh
./poc-microservices.sh
```

You have to declare a service with a *nodePort* to access each application.

Or it's possible to use an ingress controller with Istio routing features.

````bash
kubectl apply -f ingress.yml
````

Application should be exposed on *CLUSTER_IP:INGRESS_PORT*

To retrieve ingress port, use :

```bash
kubectl -n istio-system get svc istio-ingress
```