properties([[$class: 'GithubProjectProperty', displayName: '', projectUrlStr: 'https://github.com/maddinenisri/oc-jenkins-integration-pipeline/'], pipelineTriggers([githubPush()])])
node("maven") {
  echo "Pipeline Test"
  checkout scm
  checkout(
    [$class: 'GitSCM', 
     branches: [[name: '*/master']], 
     doGenerateSubmoduleConfigurations: false, 
     extensions: [], 
     submoduleCfg: [], 
     userRemoteConfigs: [[url: 'https://github.com/maddinenisri/simple-rest.git']]])
  
  sh "mvn -version"
  sh "mvn clean verify"
  
  sh "find . -name *.jar"
  
  echo "Completed"
}
