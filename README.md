# Kubernetes URL redirect

Using an nginx ingress controller that uses ConfigMap to store the nginx configuration. The nginx deployment is bootstrapped on a Kubernetes cluster using the helm package manager.

## Overview

### Install Helm
```console
curl https://raw.githubusercontent.com/helm/helm/master/scripts/get > get_helm.sh && \
chmod 700 get_helm.sh && \
./get_helm.sh
```
### Initialize Helm
```console
helm init
```
### Set service account for Helm to use
```console
kubectl create serviceaccount --namespace kube-system tiller \
kubectl create clusterrolebinding tiller-cluster-rule --clusterrole=cluster-admin --serviceaccount=kube-system:tiller \
kubectl patch deploy --namespace kube-system tiller-deploy -p '{"spec":{"template":{"spec":{"serviceAccount":"tiller"}}}}'
```
```console
$ helm install stable/nginx-ingress
```


### Building the Application

Build your application:

```

```


### Deploying


## Contributing

You don't.