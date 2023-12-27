pipeline {
    agent { docker { image 'node:20.10.0-alpine3.19' } }
    stages {
        stage('node version check') {
            steps {
                sh 'node --version'
            }
        }
		stage('clone repo'){
			steps{
				dir('some_folder'){
				checkout([$class: 'GitSCM', branches: [[name: 'main']],
				    userRemoteConfigs: [[url: 'https://github.com/imsaravana369/test-jenkins-2.git']]])

				}
				// git branch: 'main',
				// 	url: 'https://github.com/imsaravana369/test-jenkins-2.git'
			}
		}
		stage('execute code'){
			steps{
				sh 'echo hello'
			}
		}
    }
}
