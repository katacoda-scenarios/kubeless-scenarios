You can get the logs of the function

`kubeless function logs toy`{{execute}}

As well as get the description of it

`kubeless function describe toy`{{execute}}

To update a function use the `kubeless function update` command. For example to replace the toy function with the method from the `toy-udpate.py` script, do:

`kubeless function update toy --from-file toy-update.py`{{execute}}

If you check the content of the new function you will see that it hard codes the JSON object being returned:

`cat toy-update.py`{{execute}}

Under the hood, Kubernetes will do a rolling update of the Pods making up your function. Once this is finished, you can call your function and see that the new function is now deployed.

`kubeless function call toy --data '{"hello":"world"}'`{{execute}}
