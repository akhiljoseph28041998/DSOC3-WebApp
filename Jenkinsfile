pipeline {
    agent any

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

