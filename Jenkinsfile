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
        

    stages {
        stage('Run application') {
            steps {
                echo 'Hello Jenkins'

                sh 'python3 largest.py'
            }
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
