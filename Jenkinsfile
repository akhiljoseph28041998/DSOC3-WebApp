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
        stage('Build') {
            steps {
                echo 'THE PROJECT IS BUILT'
                // Print relevant environment variables
                echo "GIT_BRANCH: ${GIT_BRANCH}"
         
            }
        }
        stage('Test') {
            steps {
                echo 'THE PROJECT IS TESTED'
                // Print additional environment variables
                echo "WORKSPACE: ${WORKSPACE}"
                echo "BUILD_ID: ${BUILD_ID}"
                echo "JOB_NAME: ${JOB_NAME}"
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
