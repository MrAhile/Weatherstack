pipeline {
    agent any

    environment{
        fichierPath = "${env.WORKSPACE}"
        }

    stages {
        stage('Check Version') {
            steps {
                script {
                    docker.image('alpine/bruno').inside('--entrypoint=/bin/bash')
                    {
                        echo 'Checking Version...'
                        sh '''
                        npm -version
                        bru -version
                        '''
                        }
                }
            }
        }

        stage('Run Tests') {
            steps {
                script {
                    echo 'Running tests...'
                }
            }
        }
    }
}
