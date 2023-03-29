pipeline {
  agent any
  environment{
    Docker_Tag = getDockerTag()
  stages{
    stage('Build Docker image'){
      steps{
       bat "docker build . -t sougandhika/ubuntu:${Docker_Tag}"
      }
    }
  }
 }
}
  
  def getDockerTag(){
    def tag = bat 'git rev-parse HEAD', returnStdout: true
    return tag
  }
