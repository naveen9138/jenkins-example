pipeline {
	agent {  label 'ec2-rhel-node' }
	stages {
		stage('---clean---'){
			steps {
				tool name: 'maven3.3.3', type: 'maven'
				sh "mvn clean"
			}
		}
		stage('---test---') {
			steps {
				tool name: 'maven3.5.0', type: 'maven'
				sh "mvn test"
			}
		}
		stage('---package---'){
			steps {
				tool name: 'maven3.6.0', type: 'maven'
				sh "mvn package"
			}
		}
	}
}
