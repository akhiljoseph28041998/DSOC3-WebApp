pipeline {
    agent any  // Use any available agent to run the pipeline

    environment {
        APP_NAME = 'MY_APP'
        ENVIRONMENT = 'production'
        BUILD_VERSION = '1.0.0'
    }

    stages {
        stage('Checkout') {  // Stage to checkout code
            steps {
                git url: 'https://github.com/akhiljoseph28041998/DSOC3-WebApp.git', branch: 'main'
            }
        }

        stage('Building and Testing in Parallel') {  // Corrected stage name
            parallel {  // Parallel execution block
                "BUILDING": {
                    stage('BUILDING') {  // Stage for building the application
                        steps {
                            echo "Building the application ${APP_NAME} version ${BUILD_VERSION}..."
                            // Replace with actual build command:
                            // sh './build.sh'
                        }
                    }
                },

                "TESTING": {
                    stage('TESTING') {  // Stage for testing the application
                        steps {
                            echo "Running tests for ${APP_NAME}..."
                            // Replace with actual test command:
                            // sh './run_tests.sh'
                        }
                    }
                }
            }
        }

        stage('DEPLOYING') {  // Stage for deploying the application
            steps {
                echo "Deploying the application ${APP_NAME}..."
                // Replace with actual deploy command:
                // sh './deploy.sh'
            }
        }
    }

    post {
        success {
            echo "Pipeline completed successfully for ${APP_NAME} in ${ENVIRONMENT} environment."
        }
        failure {
            echo "Pipeline failed for ${APP_NAME} in ${ENVIRONMENT} environment."
        }
    }
}
