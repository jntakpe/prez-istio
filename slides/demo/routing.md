## Routing

Deploy a new version of *tpp-management* service :

```bash
kubectl apply -f aspsp-service-tpp-management_2.yml
```

Redirect 10% of the traffic to the new version :

```bash
istioctl delete -f routes.yml
istioctl create -f routes_v2.yml
```

Monitor that v1 is managing most of the traffic.

You can also mirror the traffic using :

```bash
istioctl delete -f routes.yml
istioctl create -f routes_mirror.yml
```

Monitor that the traffic is received by both services.