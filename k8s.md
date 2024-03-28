# K8S

`kubectl config view`

`kubectl config current-context`

`kubectl config use-context`

`kubectl explain pod.spec.restartPolicy`

Restart policy applies on container within Pod not on the Pod. Pod alwayes deleted and created new.

`kubectl get pods hello-pod -o yaml`

`kubectl describe pod hello-pod`
