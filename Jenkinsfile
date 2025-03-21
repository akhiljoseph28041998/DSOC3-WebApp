pipeline {
    agent any

    environment{
        ENV_VAR1 = 'env var-1 value'
        ENV_VAR2 = 'env var-2 value'
        ENV_VAR3 = 'env var-3 value'
        ENV_VAR4 = 'env var-4 value'
    }

    stages {
        stage('Build') {
            steps {
                echo 'THE PROJECT IS BUILD'
            }
        }
        stage('Test') {
            steps {
                echo 'THE PROJECT IS TESTED'
            }
            post {
                always {
                    echo 'This runs always stage test'
                }
                success {
                    echo 'This runs on success stage test'
                }
                failure {
                    echo 'This runs on failure stage test'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'THE PROJECT IS DEPLOYED'
            }
        }
    }
}

