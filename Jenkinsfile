
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Test Application') {
            steps {
                sh 'python3 -m py_compile app.py'
                echo 'Python syntax test passed!'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t student-todo:latest .'
            }
        }
    }
}
