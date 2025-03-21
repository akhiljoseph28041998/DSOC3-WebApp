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
                echo "BRANCH_IS_PRIMARY: ${BRANCH_IS_PRIMARY}"
                echo "CHANGE_ID: ${CHANGE_ID}"
                echo "CHANGE_URL: ${CHANGE_URL}"
                echo "CHANGE_AUTHOR_DISPLAY_NAME: ${CHANGE_AUTHOR_DISPLAY_NAME}"
                echo "CHANGE_AUTHOR_EMAIL: ${CHANGE_AUTHOR_EMAIL}"
                echo "CHANGE_TARGET: ${CHANGE_TARGET}"
                echo "CHANGE_BRANCH: ${CHANGE_BRANCH}"
                echo "CHANGE_FORK: ${CHANGE_FORK}"
                echo "TAG_NAME: ${TAG_NAME}"
                echo "TAG_TIMESTAMP: ${TAG_TIMESTAMP}"
              
                
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
