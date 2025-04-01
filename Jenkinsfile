pipeline {
    agent any  // Use any available agent to run the pipeline

    stages {
        stage('Checkout') {  // Stage to checkout code
            steps {
                git url: 'https://github.com/akhiljoseph28041998/DSOC3-WebApp.git', branch: 'main'
            }
        }
        
        stage('BUILDING') {  // Stage for building the application
            steps {
                echo 'Building stages'
                // Add your actual build commands here, like:
                // sh './build.sh'
            }
        }

        stage('TESTING') {  // Stage for testing the application
            steps {
                echo 'Testing stages'
                // Add your actual test commands here, like:
                // sh './run_tests.sh'
            }
        }

        stage('DEPLOYING') {  // Stage for deploying the application
            steps {
                echo 'Deploying stages'
                // Add your actual deploy commands here, like:
                // sh './deploy.sh'
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
