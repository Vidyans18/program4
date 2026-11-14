
pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Checking Python application'

                bat '"C:\\Users\\student\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" --version'

                bat '"C:\\Users\\student\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" -m unittest app'
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
