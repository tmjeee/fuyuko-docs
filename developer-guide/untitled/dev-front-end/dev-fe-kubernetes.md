# Dev - FE - Kubernetes

{% hint style="info" %}
You will need Kubernetes environment setup first. [Digital Ocean](www.digitalocean.com), [Google](http://cloud.google.com), [Amazon](http://aws.amazon.com) and [Azure](https://azure.microsoft.com/) all offer Kubernetes services
{% endhint %}

Kubernetes scripts and yaml configuration files are located in.

```text
+ <root>/
    + kubernetes/
        ... all kubernetes scripts and yaml files ...
```

{% hint style="info" %}
Following sections' code snippet assume you are located in `<root>/kubernetes/` directory
{% endhint %}

## config.json as a Kubernetes ConfigMap

Run script `k8s-fuyuko-fe-config.sh` file to have `config.json` located in \(`/assets/config.json` in docker image\) to be configured as a **Kubernetes Config Map**, allowing it to be configured independently.

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

## Running a FE kubernetes deployment

Run the following command to have a FE kubernetes deployment installed

```text
$> kubectl apply -f ./k8s-fuyuko-fe-deployment.yaml
```

