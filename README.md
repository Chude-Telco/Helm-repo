# Helm-repo Helloworld deployed using Helm v3.2.1 and Kubernetes cluster version v1.18.1
[sysadmin@controller-0 hello-app(keystone_admin)]$ helm install hello-app-2.0.0.tgz --generate-name
NAME: hello-app-2-1631205188
LAST DEPLOYED: Thu Sep  9 16:33:10 2021
NAMESPACE: default
STATUS: deployed
REVISION: 1
NOTES:
1. Get the application URL by running these commands:
  export NODE_PORT=$(kubectl get --namespace default -o jsonpath="{.spec.ports[0].nodePort}" services hello-app-2-1631205188)
  export NODE_IP=$(kubectl get nodes --namespace default -o jsonpath="{.items[0].status.addresses[0].address}")
  echo http://$NODE_IP:$NODE_PORT
