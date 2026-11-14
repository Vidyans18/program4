pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage ('Build') {
            steps {
                echo 'checking Python application'
                bat 'python -m unittest app'
            }
        }
        
        stages ('Run application') { 
         steps {
                echo 'Running Python application'

                sh 'python3 app.py'
            }
        }
    }
    
    post {
        success {
            echo 'CI pipeline completed successfully'
        }
        failure {
            echo 'CI pipeline failed'
        }
    }
}
