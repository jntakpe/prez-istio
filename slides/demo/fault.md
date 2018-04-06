## Fault injection

Delay responses using :

```bash
istioctl delete -f routes_mirror.yml
istioctl create -f routes_delay.yml
```

Monitor that the traffic going to v2 service is delayed

Inject faults using :

```bash
istioctl delete -f routes_delay.yml
istioctl create -f routes_fault.yml
```

Monitor that the traffic going to v1 service is failing