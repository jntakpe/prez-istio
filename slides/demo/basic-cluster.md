## Kubernetes cluster resiliency

Check that applications are available then replace *tpp-management* with a faulty version.

```bash
kubectl delete -f aspsp-service-tpp-management.yml
kubectl apply -f aspsp-service-tpp-management_fail.yml
```

Check that the cluster is working as expected then force *tpp-management* to fail using endpoint : */tpps/fail/{duration}*

```bash
curl -X POST -H "Authorization: $BEARER_TOKEN" http://CLUSTER_IP:30180/api/tpps/fail/30
```

Check the results using *PSU auth direct* JMeter thread group.