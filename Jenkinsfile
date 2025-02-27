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
                bat 'echo %PATH%'
                bat 'set PATH=C:\\Path\\To\\Your\\Python;%PATH% && python -c "from button import click; click()"'
            }
        }
        stage('Test NewScreen') {
            steps {
                bat 'set PATH=C:\\Path\\To\\Your\\Python;%PATH% && python -c "from screen import welcome; welcome()"'
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
