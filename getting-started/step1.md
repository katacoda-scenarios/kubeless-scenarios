Create a _kubeless_ namespace where you will install the controller.

`kubectl create ns kubeless`{{execute}}

Install the latest stable version with a `kubectl create` command

`kubectl create -f https://github.com/kubeless/kubeless/releases/download/v1.0.0-alpha.8/kubeless-v1.0.0-alpha.8.yaml`{{execute}}

You can see that a few pods are being started in the _kubeless_ namespace. The controller which will watch for function objects to be created and also two Pods to enabled PubSub function.

`kubectl get pods -n kubeless`{{execute}}

As soon as the controller starts you can deploy a function. In this getting started guide you do not need to wait for the other pods to start. HTTP triggered functions are available right away.
