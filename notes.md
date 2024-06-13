for ratings micro service we are using in-memory data store redis(reason: ratings may vary from time-to-time and if we use some db in-place of redis there will be some latency).
Most of the times redis is created as stateful sets and it is connected to persistent  volume (reason : lets say for some reason redis goes down)

# how to deploy micro-services to k8s cluster

1. containerize the application---> create manisfests---> deploy deployments.yaml & service.yaml onto k8s cluster.

2. containerize(using dockerfile) the application ---> we need to create k8s manifests file ----> we need to conver them to helm charts ----> we need to these charts to k8s cluster.

components of helm charts 

charts.yaml

templates(inside this we will be placing all the manifest files)

values.yaml

azure files(efs)
azure disks(ebs)

if we create a stateful set with pvc 


