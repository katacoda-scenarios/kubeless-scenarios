Note that any Openfaas function will run in kubeless:

`kubeless function deploy --runtime-image functions/markdownrender markdownrender`{{execute}}

And call it:

`kubeless function call --data '{"a": "aa"}' markdownrender`{{execute}}

Once you are done you can remove the functions

`kubeless function delete toy`{{execute}}

and 

`kubeless function delete hello`{{execute}}

The deployment and Kubernetes services will be removed automatically

`kubectl get deployments,services`{{execute}}
