# Overview

This chart is a simple demonstration on how envoyproxy and lyft ratelimit work

## How To Install

```bash
git clone https://github.com/rudydydy/envoy-ratelimit-helm-chart
cd envoy-ratelimit-helm-chart
helm install envoy-ratelimit .
```

After installed try to get the envoy LoadBalancer IP

```bash
ENVOY_IP=$(kubectl get svc envoy-ratelimit --output jsonpath='{.status.loadBalancer.ingress[0].ip}')
open http://$ENVOY_IP
```

Then open 

## References

Envoy configuration [reference](https://www.envoyproxy.io/docs/envoy/latest/)
