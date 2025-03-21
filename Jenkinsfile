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
                    echo 'This runs always'
                }
                success {
                    echo 'This runs on success'
                }
                failure {
                    echo 'This runs on failure'
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
