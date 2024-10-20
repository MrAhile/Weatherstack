pipeline {
    agent {
        any {
            image 'node:14'  // Use the official Node.js 14 Docker image (or specify the version you need)
            args '-v /var/run/docker.sock:/var/run/docker.sock'  // Allow Docker in Docker if needed
        }
    }

    stages {
        stage('Install Dependencies') {
            steps {
                script {
                    echo 'Installing dependencies...'
                    sh 'npm install'  // Install Node.js dependencies using npm
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    echo 'Running tests...'
                    sh 'npm --version'  // Run tests using npm
                }
            }
        }
    }
}
