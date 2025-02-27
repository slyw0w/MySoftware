pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Test NewButton') {
            steps {
                sh 'python3 -c "from button import click; click()"'
            }
        }
        stage('Test NewScreen') {
            steps {
                sh 'python3 -c "from screen import welcome; welcome()"'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}