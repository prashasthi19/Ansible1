pipeline{
	agent any
	tools{
		maven 'maven'
	}
	stages{
		stage('Checkout'){
			steps{
				git branch:'master', url:'https://github.com/prashasthi19/Ansible1.git'
			}
		}
		stage('Build'){
			steps{
				sh 'mvn clean install'
			}
		}
		stage('Test'){
			steps{
				sh 'mvn test'
			}
		}
		stage('Run Application'){
			steps{
				sh 'java -jar target/Ansible1-1.0-SNAPSHOT.jar'
			}
		}
	}
}

