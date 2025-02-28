pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git(url: 'https://github.com/slyw0w/MySoftware.git', branch: 'main')
            }
        }
        stage('Run Tests') {
            steps {
                echo "Running tests..."
                sh """python3 button.py"""
                sh """python3 screen.py"""
            }
        }
    }
}
