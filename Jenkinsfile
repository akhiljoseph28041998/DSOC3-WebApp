pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'THE PROJECT IS BUILD'
            }
        }
        stage('test') {
            steps {
                echo 'THE PROJECT IS tested'
            }
        }
         stage('deploy') {
            steps {
                echo 'THE PROJECT IS deploye'
            }
        }
 }
post{
        always{
            echo 'this run always'
        }
        success{
            echo 'this run on success'
        }
        failure{
            echo 'this run failed'
        }
    }
}
