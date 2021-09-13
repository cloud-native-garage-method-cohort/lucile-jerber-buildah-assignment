# Buildah assignment

See course : https://github.com/cloud-native-garage-method-cohort/emea-5-ci-cd-from-first-principles/blob/main/tekton/pipeline-build-03-buildah.md

1. Create git repo
2. Create quay repo
3. Change values in pipelune-run.yaml with new repo 

## Quay credentials
1. In new repo go to settings
2. Add a new robot user with write permissions

## Tasks install:
*NPM*
kubectl apply -f https://raw.githubusercontent.com/tektoncd/catalog/main/task/npm/0.1/npm.yaml

*Buildah*
oc get clustertasks | grep -i buildah

## In folder tekton :*

oc apply -f base 
oc create -f pipeline-run.yaml

*Go to the openshift cluster console to check the status of your pipeline :*

oc console