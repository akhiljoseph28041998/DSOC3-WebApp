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
        stage('Build') {
            steps {
                echo 'THE PROJECT IS BUILT'
                echo "GIT_BRANCH : ${GIT_BRANCH}"
                echo "JENKINS_HOME: ${JENKINS_HOME}"
            }
        }
        stage('Test') {
            steps {
                echo 'THE PROJECT IS TESTED'
                echo "WORKSPACE: ${WORKSPACE}"
                echo "BUILD_ID:${BUILD_ID}"
                echo "JOB_NAME:${JOB_NAME}"
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
