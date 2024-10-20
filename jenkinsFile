pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout csm
            }
        }

        stage('Install NPM and Bruno CLI') {
            steps {
                script {
                    // Build Docker image using Docker CLI
                    sh '''
                    ls .
                    npm install
                    npm install -g @usebruno/cli
                    '''
                }
            }
        }

        stage('Run Bruno Commands') {
            steps {
                script {
                    // Running shell commands
                    sh '''
                    bru run --version
                    '''
                }
            }
        }
    }
}
