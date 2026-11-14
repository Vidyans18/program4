
pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out GitHub repository'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Checking Python application'

                bat '"C:\\Users\\student\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" --version'

                bat '"C:\\Users\\student\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" -m py_compile largest.py'
            }
        }

        stage('Run application') {
            steps {
                echo 'Hello Jenkins'

                bat '"C:\\Users\\student\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" largest.py'
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
