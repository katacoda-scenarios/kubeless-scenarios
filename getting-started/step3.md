You can call the function using the kubeless CLI convenience wrapper:

`kubeless function call toy --data '{"hello":"world"}'`{{execute}}

Or you can call the service endpoint if you have a proxy running.

Let's run a proxy:

`kubectl proxy --port 8080 &`{{execute}}

And now let's call the function directly via _curl_:

`curl --data '{"hello":"world"}' localhost:8080/api/v1/namespaces/default/services/toy:8080/proxy/ --header "Content-Type:application/json"`{{execute}}
