pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/<username>/devops-demo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                bat 'dir'
                bat 'python app.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'python -m py_compile app.py'
            }
        }
    }
}
