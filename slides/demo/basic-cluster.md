## Kubernetes cluster resiliency

Start Kafka and microservices using :

```bash
./poc-infra.sh
./poc-microservices.sh
```

Check that applications are available then replace *tpp-management* with a faulty version.

```bash
kubectl delete -f aspsp-service-tpp-management.yml
kubectl apply -f aspsp-service-tpp-management_fail.yml
```

Check that the cluster is working as expected.

Force the failure of the *tpp management* service :  

```bash
curl -X POST -H "Authorization: $BEARER_TOKEN" http://CLUSTER_IP:30180/api/tpps/fail/30
```

Check the results using *PSU auth direct* JMeter thread group.