## Control egress traffic

Initialize configuration :

```bash
./minikube-istio.sh
./update-ip.sh
kubectl apply -f config-map.yml
```

Start application **server-config** :

````bash
kubectl apply -f server-config.yml
````

Application should not start

Add egress rule :

````bash
kubectl apply -f egress.yml
````

Application should start now