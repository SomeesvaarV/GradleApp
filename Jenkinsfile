pipeline{
	agent any
	
	tools{
		gradle 'Gradle'
		jdk 'JDK'
	}
	
	stages{
		stage('Checkout'){
			steps{
				git branch:'main', url:'https://github.com/SomeesvaarV/GradleApp.git'
			}
		}
		stage('Build'){
			steps{
				sh 'gradle build' 
			}
		}
		stage('Test'){
			steps{
				sh 'gradle test' 
			}
		}
		stage('run'){
			steps{
				sh 'gradle run' 
			}
		}
	}
	
	post{
		success{
			echo 'Build and Deployment Successful'
		}
		failure{
			echo 'Builed failed'
		}
	}
}
