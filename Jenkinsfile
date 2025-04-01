pipeline {
    agent any  // Use any available agent to run the pipeline

    stages {
        stage('Checkout') {  // Stage to checkout code
            steps {
                git 'https://github.com/akhiljoseph28041998/DSOC3-WebApp.git'
                branch: 'main'
            }
        stage('BUILDING') {  // You need to name the stage
            steps {
                // Add your steps here
                echo 'building stages'
            }
        }
         stage('TESTING') {  // You need to name the stage
            steps {
                // Add your steps here
                echo 'testing stages'
            }
        }
         stage('DEPLOYE') {  // You need to name the stage
            steps {
                // Add your steps here
                echo 'deploying stages'
            }
        }
    }
    post{
        success{
            echo "pipeline  complited successfuly "
        }
        failure{
            echo "pipleline failure" 
        }
    }
}
