## Istio resiliency

Apply Istio circuit breaker policy and force *tpp-management* to fail :

```bash
istioctl create -f tpp-management_cb.yml
curl -X POST -H "Authorization: $BEARER_TOKEN" http://CLUSTER_IP:30180/api/tpps/fail/30
```

Check the results using *PSU auth direct* JMeter thread group.

Apply Istio retry policy and force *tpp-management* to fail :

```bash
istioctl create -f tpp-management_retry.yml
curl -X POST -H "Authorization: $BEARER_TOKEN" http://CLUSTER_IP:30180/api/tpps/fail/30
```

Check the results using *PSU auth direct* JMeter thread group.