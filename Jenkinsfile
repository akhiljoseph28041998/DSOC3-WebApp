pipeline {
    agent any

    environment {
        ENV_VAR1 = 'env var-1 value'
        ENV_VAR2 = 'env var-2 value'
        ENV_VAR3 = 'env var-3 value'
        ENV_VAR4 = 'env var-4 value'
    }

    stages {
        stage('Build') {
            steps {
                echo 'THE PROJECT IS BUILT'
                //echo "The value of the environment variable: ${ENV_VAR1}"
                sh 'echo The value of the environment variable: ${ENV_VAR1}'
            }
        }
        stage('Test') {
            steps {
                echo 'THE PROJECT IS TESTED'
                //echo "The value of the environment variable: ${ENV_VAR2}"
                sh 'echo The value of the environment variable: ${ENV_VAR2}'
            }
            post {
                always {
                    echo 'This runs always in the Test stage'
                }
                success {
                    echo 'This runs on success in the Test stage'
                }
                failure {
                    echo 'This runs on failure in the Test stage'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'THE PROJECT IS DEPLOYED'
                //echo "The value of the environment variable: ${ENV_VAR3}"
                sh 'echo The value of the environment variable: ${ENV_VAR3}'
            }
        }
    }
}
