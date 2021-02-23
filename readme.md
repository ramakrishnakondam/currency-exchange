instructions to deploy currency exchange and currency conversion microservices to AWS EKS cluster

Step 1:
In your aws account using eksctl create a K8S cluster
eksctl create cluster
this takes a while to provision and it creates a K8S cluster with 2 worker nodes.

Step 2:
Deploy the currency exchange and currecny conversion microservices using the deployment.yaml files created
use kubectl get pods to check if pods are up and running

Step 3:
To handle incoming traffic we need to deploy an ingress controller, most commoly used is nginx ingress controller.
https://kubernetes.github.io/ingress-nginx/

Step 4:
After the ingress controller is deployed to the cluster we need to deploy an ingress resource as defined in ingress.yaml