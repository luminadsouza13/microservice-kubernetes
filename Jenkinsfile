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
	stage('Local tests') {
		steps{
	}

	}
	stage('Publish Docker') {
			steps{
	}
	}
	stage('Deploy to dev') {
			steps{
	}
	}
	stage('Dev tests') {
			steps{
	}
	}
	stage('Cleanup dev') {
			steps{
	}
	}
	stage('Deploy to staging') {
			steps{
	}
	}
	stage('Staging tests') {
			steps{
	}
	}
	stage('Cleanup staging') {
			steps{
	}
	}
	////////// Step 6 //////////
    // Waif for user manual approval, or proceed automatically if DEPLOY_TO_PROD is true
   stage('Go for Production?') {
			steps{
	}
	}
}


}
