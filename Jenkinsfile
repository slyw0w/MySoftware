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
                bat 'python -c "from button import click; click()"'
            }
        }
        stage('Test NewScreen') {
            steps {
                bat 'python -c "from screen import welcome; welcome()"'
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
