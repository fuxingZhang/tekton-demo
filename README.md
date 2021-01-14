# tekton-knative
tekton knative auto deploy demo

```bash
# secret 
kubectl apply -f ./image-secret.yaml
kubectl delete -f ./image-secret.yaml
# account
kubectl apply -f ./pipeline-account.yaml
kubectl delete -f ./pipeline-account.yaml

# git resources
kubectl apply -f ./resources/picalc-git.yaml
kubectl delete -f ./resources/picalc-git.yaml

kubectl apply -f ./tasks/deploy-using-kubectl.yaml  
kubectl apply -f ./tasks/source-to-image.yaml
kubectl apply -f ./pipeline/build-and-deploy-pipeline.yaml
kubectl apply -f ./run/picalc-pipeline-run.yaml

kubectl delete -f ./tasks/deploy-using-kubectl.yaml  
kubectl delete -f ./tasks/source-to-image.yaml
kubectl delete -f ./run/picalc-pipeline-run.yaml
kubectl delete -f ./pipeline/build-and-deploy-pipeline.yaml

```