pipeline {
    agent any  // Use any available agent to run the pipeline

    stages {
        stage('Checkout') {  // Stage to checkout code
            steps {
                git url: 'https://github.com/akhiljoseph28041998/DSOC3-WebApp.git', branch: 'main'
            }
        }
        
        stage('Building and Testing in Parallel') {  // Corrected stage name
            parallel {  // Corrected 'parallel' syntax
                stage('BUILDING') {  // Stage for building the application
                    steps {
                        echo 'Building the application...'
                        // Add your actual build command here, e.g., sh './build.sh'
                    }
                }

                stage('TESTING') {  // Stage for testing the application
                    steps {
                        echo 'Running tests...'
                        // Add your actual test command here, e.g., sh './run_tests.sh'
                    }
                }
            }
        }

        stage('DEPLOYING') {  // Stage for deploying the application
            steps {
                echo 'Deploying the application...'
                // Add your actual deploy command here, e.g., sh './deploy.sh'
            }
        }
    }

    post {
        success {
            echo "Pipeline completed successfully"
        }
        failure {
            echo "Pipeline failed"
        }
    }
}
