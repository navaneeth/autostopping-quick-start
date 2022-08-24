# AutoStopping quick start

This repository provides a sample HTTP application and it's associated AutoStopping rule configuration to quickly try out AutoStopping. 

# Install the sample application

```
kubectl apply -f https://raw.githubusercontent.com/navaneeth/autostopping-quick-start/main/sample-app.yml
```

This will install a demo application named `autostopping-sample` which runs 3 pods running `nginx`. It also creates a k8s Service and Ingress. If your cluster is not using Ingress, modify the code to remove Ingress configuration

# Install the AutoStopping rule

Before applying, ensure the cloud connector id is updated and the namespace is same as the `autostopping-sample` application

```
wget https://raw.githubusercontent.com/navaneeth/autostopping-quick-start/main/as-rule.yml
# replace harness.io/cloud-connector-id: Lightwing_Non_Prod to a valid cloud connector id (AWS/GCP/Azure)
kubectl apply -f as-rule.yml
```
