# HPA Example

Heavily inspired by a [DigitalOcean Blog](https://www.digitalocean.com/community/tutorials/how-to-configure-kubernetes-horizontal-pod-autoscaler-using-metrics-server).

```shell
# create app
oc create -f ./app.yaml

# see logs
# stern --selector=run=python-constant-load-test

# create hpa
oc create -f ./hpa.yaml
```

If the average cpu utilization is 50% (or more) of the requested CPU, then we
will scale up. For this example application, this will happen.
