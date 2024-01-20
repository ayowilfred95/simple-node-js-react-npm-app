pipeline {
    agent any

    environment {
        DOCKER_TLS_VERIFY = '1'
        DOCKER_CERT_PATH = '/Users/wilfred/.docker/desktop'
        DOCKER_HOST = 'tcp://localhost:2376'
    }

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:14-alpine'
                    args '-p 3000:3000' 
                }
            }

            steps {
                sh 'npm install'
            }
        }
    }
}
