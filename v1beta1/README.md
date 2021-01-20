# tekton-knative
tekton knative auto deploy demo

```bash
# image secret 
kubectl create -f ./image-secret.yaml
kubectl delete -f ./image-secret.yaml

# minio secret
kubectl create -f ./minio-secret.yaml
kubectl delete -f ./minio-secret.yaml

# account
kubectl create -f ./pipeline-account.yaml
kubectl delete -f ./pipeline-account.yaml

# Tasks
kubectl create -f ./Tasks/fetch-build-push.yaml
kubectl create -f ./Tasks/deploy-using-kubectl.yaml  

# TaskRuns
kubectl create -f ./TaskRuns/fetch-build-push.yaml
kubectl create -f ./TaskRuns/deploy-using-kubectl.yaml

# Pipelines
kubectl create -f ./Pipelines/build-and-deploy.yaml

# PipelineRuns
kubectl create -f ./PipelineRuns/build-and-deploy.yaml

# delete
kubectl delete -f ./Tasks/fetch-build-push.yaml
kubectl delete -f ./Tasks/deploy-using-kubectl.yaml  
kubectl delete -f ./Pipelines/build-and-deploy.yaml
kubectl delete -f ./PipelineRuns/build-and-deploy.yaml
```