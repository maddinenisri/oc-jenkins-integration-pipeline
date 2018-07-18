# oc-jenkins-integration-pipeline

## Test for Openshift Integration

### Trying with webhook to Jenkins url

## Need access to list PODS 
oc policy add-role-to-user edit system:serviceaccount:demo:default -n demo

oc adm policy add-scc-to-user anyuid -z default

http://jenkins.demo.svc.cluster.local:8080
jenkins-jnlp.demo.svc.cluster.local:50000

maven
jnlp
docker.io/openshift/jenkins-agent-maven-35-centos7:v3.11
/tmp
${computer.jnlpmac} ${computer.name}


properties([pipelineTriggers([githubPush()])])

node {
    git url: 'https://github.com/maddinenisri/oc-jenkins-integration-pipeline.git', branch: 'master'
}
