pipeline {
    agent { docker { image 'node:20.10.0-alpine3.19' } }
    stages {
        stage('node version check') {
            steps {
                sh 'node --version'
            }
        }
		stage('execute code'){
			steps{
				git branch: 'main',
					url: 'https://github.com/imsaravana369/test-jenkins-2.git'
				sh 'cd My-First-Pipeline_main && npm run start'
			}
		}
    }
}
