** This section is a WIP **

Apologies, this is a work in progress. But, we've made a quick video to get you started!

# Video

[Istio Routing to Enable ML DevOps Workflows](https://youtu.be/ZcdEdAi-tSw)

# Steps

in istio


https://istio.io/docs/setup/kubernetes/quick-start/

install

```
curl -L https://git.io/getLatestIstio | sh -
cd istio-0.8.0
export PATH=$PWD/bin:$PATH
helm install install/kubernetes/helm/istio --name istio --namespace istio-system
```
Verify 
```
kubectl get svc -n istio-system
```

Enable

```
kubectl label namespace default istio-injection=enabled
kubectl get namespace -L istio-injection
```


- deploy a sample helm a couple of times, increment the build number and mout path in the values.yaml each time. 




- kubectl apply -f svc.yaml
- istioctl create -f gateway.yaml
- kubectl apply -f nginx/frontend.yaml
- istioctl create -f front-virtual-service.yaml
- istioctl create -f back-virtual-service.yaml
- 

kubectl get svc istio-ingressgateway -n istio-system


istioctl get virtualservices


service graph: https://istio.io/docs/tasks/telemetry/servicegraph/
