pipeline {
    agent any
    

    stages {
        stage('Print ENV') {
            steps {
                echo 'THE PROJECT IS BUILD'
                // Print all environment variables
                sh 'printenv'
            }
        }
         stage('front-end-code') {
            steps {
                echo 'THE PROJECT IS BUILD'
                sh"git clone..."
               
            }
        }
         stage('backend-code') {
            steps {
                echo 'THE PROJECT IS BUILD'
                 sh"git clone..."
                
            }
        }
        stage('Build') {
            steps {
                echo 'THE PROJECT IS BUILT'
                
         
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
