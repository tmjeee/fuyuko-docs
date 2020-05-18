# Dev - BE - Kubernetes

{% hint style="info" %}
You will need Kubernetes environment setup first. [Digital Ocean](www.digitalocean.com), [Google](http://cloud.google.com), [Amazon](http://aws.amazon.com) and [Azure](https://azure.microsoft.com/) all offer Kubernetes services
{% endhint %}

Kubernetes scripts and yaml configuration files are located in 

```text
+ <root>/
    + kubernetes/
        ... all kubernetes scripts and yaml files ...
```

{% hint style="info" %}
Following sections' code snippet assume you are located in `<root>/kubernetes/` directory
{% endhint %}

## config.json as Kubernetes ConfigMap

Run script `k8s-fuyuko-be-config.sh` file to have `config.json` located in \(`/src/config/config.json` in docker image\) to be configured as a **Kubernetes Config Map**, allowing it to be configured independently.

```text
$> ./k8s-fuyuko-be-config.sh 
```

Once this is ran successfully, you should be able to see fuyuko-be-config configmaps listed when the following command is ran.

```text
$> kubectl get configmaps
```

Edit `fuyuko-be-config` config map to suits your environment using :

```text
$> kubectl edit configmaps fuyuko-be-config 
```

## Running a BE kubernetes deployment

Run the following command to have a FE kubernetes deployment installed

```text
$> kubectl apply -f ./k8s-fuyuko-be-deployment.yaml
```

Deployment and pods should be listed when running the following command respectively

```text
$> kubectl get deployments
```

```text
$> kubectl get pods
```

## Installing a Load Balancer for BE deployment

### With HTTPS

{% hint style="info" %}
Edit k8s-fuyuko-be-loadbalancer.yaml and put in your HTTPS certificate id, this will need to be configured in your provider environment which differs between providers.

```text
metadata:
  ...
  annotations:
    ...
    service.beta.kubernetes.io/do-loadbalancer-certificate-id: "Your SSL Certificate ID"

```
{% endhint %}

### Without HTTPS

{% hint style="info" %}
Edit k8s-fuyuko-be-loadbalancer.yaml and remove the following lines from the `annotations` section

```text
service.beta.kubernetes.io/do-loadbalancer-tls-ports: "8443"
service.beta.kubernetes.io/do-loadbalancer-certificate-id: "..."
```
{% endhint %}

### Apply load balancer yaml configurations

Install the load balancer by running the followings

```text
$> kubectl apply -f ./k8s-fuyuko-be-loadbalancer.yaml
```

Upon successful installation, your loadbalancer should appear when the following command is ran

```text
$> kubectl get services
```



