# K8S

`kubectl config view`

`kubectl config current-context`

`kubectl config use-context`

`kubectl explain pod.spec.restartPolicy`

Restart policy applies on container within Pod not on the Pod. Pod alwayes deleted and created new.

`kubectl get pods hello-pod -o yaml`

`kubectl describe pod hello-pod`

`kubectk logs <pod>`

`kubectl exec <pod> -- command` example `kubectl exec hello-pod -- curl localhost:8080`


`kubectl exec -it hello-pod -- sh` it interactive


`metadata > name` is pod hostname. 

Resource Request: Min values
Resource Limit: Max values

Multi-container pods: init container, sidecar container


