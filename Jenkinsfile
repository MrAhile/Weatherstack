pipeline {
    agent any

    environment{
        fichierPath = "${env.WORKSPACE}"
        }

    stages {
        stage('Run Tests') {
            steps {
                script {
                    echo 'Running tests...'
                    echo '${fichierPath}'
                }
            }
        }

        stage('Run Build') {
            steps {
                script {
                    echo 'Running Builds...'
                }
            }
        }
    }
}
