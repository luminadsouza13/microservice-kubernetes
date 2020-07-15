pipeline{

// In this example, all is built and run from the master
agent { docker 'maven:3-alpine' }
stages{
	stage('Git clone and setup'){
		steps{
			echo "Check out code"
			git branch: "master", credentialsId: 'cred2', url: 'https://github.com/eldada/jenkins-pipeline-kubernetes.git'
			
			sh "kubectl cluster-info"
			
		}
	}
	stage('Build and tests') {
		steps{
			echo "Building application and Docker image"
			sh "mvn clean package"	
		}
	}

	}
}
