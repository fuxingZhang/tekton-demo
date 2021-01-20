# tekton-knative
tekton knative auto deploy demo

```bash
# secret 
kubectl create -f ./image-secret.yaml
kubectl create -f ./minio-secret.yaml
kubectl delete -f ./image-secret.yaml
kubectl delete -f ./minio-secret.yaml

# account
kubectl create -f ./pipeline-account.yaml
kubectl delete -f ./pipeline-account.yaml

# git resources
kubectl create -f ./resources/picalc-git.yaml
kubectl delete -f ./resources/picalc-git.yaml

kubectl create -f ./tasks/source-to-image.yaml
kubectl create -f ./tasks/deploy-using-kubectl.yaml  
kubectl create -f ./pipeline/build-and-deploy-pipeline.yaml
kubectl create -f ./run/picalc-pipeline-run.yaml

kubectl delete -f ./tasks/source-to-image.yaml
kubectl delete -f ./tasks/deploy-using-kubectl.yaml  
kubectl delete -f ./pipeline/build-and-deploy-pipeline.yaml
kubectl delete -f ./run/picalc-pipeline-run.yaml
```