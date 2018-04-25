To deploy a function you use the `kubeless` CLI. You need to specify a _runtime_ which specifies which language your function is in. You need to specify the file that contains your function, how the function will get triggered (here we use an HTTP trigger) and finally you specify the function name as a _handler_.

`kubeless function deploy toy --runtime python2.7 \
                              --handler toy.handler \
                              --from-file toy.py`{{execute}}

You can then list the function with the `kubeless` CLI:

`kubeless function ls`{{execute}}

While the function get deployed you can check the actual Python function:

`cat toy.py`{{execute}}

Under the hood, Kubeless automatically created a Kubernetes deployment and service. You can check that a Pod containing your function is running:

`kubectl get pods`{{execute}}
