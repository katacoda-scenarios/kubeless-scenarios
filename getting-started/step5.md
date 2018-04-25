There are additional runtimes. In addition to Python 2.7 and 3.4 you can also deploy Ruby, Node and .Net core functions.

Let's deploy a toy Node.js function.

`cat hello.js`{{execute}}

You can deploy this function like so:

`kubeless function deploy hello --runtime nodejs6 \
                              --handler hello.handler \
                              --from-file hello.js`{{execute}}

You can list it

`kubeless function ls`{{execute}}

And call it as well

`kubeless function call hello --data '{"kubeless":"rocks"}'`{{execute}}

