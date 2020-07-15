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
		echo "Building application and Docker image"
		sh "mvn clean package"	
	}
	stage('Local tests') {
	}
	stage('Publish Docker') {
	}
	stage('Deploy to dev') {
	}
	stage('Dev tests') {
	}
	stage('Cleanup dev') {
	}
	stage('Deploy to staging') {
	}
	stage('Staging tests') {
	}
	stage('Cleanup staging') {
	}
	////////// Step 6 //////////
    // Waif for user manual approval, or proceed automatically if DEPLOY_TO_PROD is true
   stage('Go for Production?') {
   }

}


}
