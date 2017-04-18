`kubectl create -f function.yaml`{{execute}}

`kubectl get pods`{{execute}}

`kubeless function call function`{{execute}} <<--fails.

Loading /kubeless/hello.js
mod[funcHandler] handler undefined
