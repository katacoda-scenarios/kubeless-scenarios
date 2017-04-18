`kubeless function deploy toy --runtime python27 \
                              --handler toy.foobar \
                              --from-file toy.py \
                              --trigger-http`{{execute}}

`kubectl get functions`{{execute}}

`kubeless function ls`{{execute}}
