 pipeline {
  agent {
   docker{
    image 'maven:3-alpine'
   }
  }
  stages {
    stage('Build') {
      steps {
        sh 'cd microservice-kubernetes-demo'
        sh './mvnw clean package'
      }
    }

  }
}
