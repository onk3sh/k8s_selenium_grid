# Kubernetes Selenium Grid setup using Google Container Registry in GCP

Launching selenium hub as a service
```
$ kubectl create -f selenium-hub-deployment.yaml
```

Lets create a service for nodes to connect to,
```
$ kubectl create -f selenium-hub-svc.yaml
```

Spin up Chrome Nodes
Now since hub is up and exposed lets spin up nodes and register into hub
```
$ kubectl create -f selenium-node-chrome-deployment.yaml
```
Now nodes are up and registered to hub created above can be seen in exposed selenium-hub’s console.
