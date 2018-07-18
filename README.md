# oc-jenkins-integration-pipeline

## Test for Openshift Integration

### Trying with webhook to Jenkins url

## Need access to list PODS 
oc policy add-role-to-user edit system:serviceaccount:demo:default -n demo

oc adm policy add-scc-to-user anyuid -z default
