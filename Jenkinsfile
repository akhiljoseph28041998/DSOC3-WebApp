pipeline {
    agent any

    stages {
        stage('Print ENV') {
            steps {
                echo 'THE PROJECT IS BUILD'
                // Use 'printenv' to print all environment variables
                sh 'printenv'
            }
        }
        stage('Parallel Stages') {
            parallel {
                stage('Build') {
                    steps {
                        echo 'THE PROJECT IS BUILT'
                    }
                }
                stage('Test') {
                    steps {
                        echo 'THE PROJECT IS TESTED'
                    }
                }
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
