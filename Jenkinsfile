pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/slyw0w/MySoftware.git', branch: 'main'
            }
        }
        stage('Test Button') {
            steps {
                bat '''
                "C:\Users\nyyif\AppData\Local\Programs\Python\Python39\python.exe" -c "import button; button.click(); print('Button test passed')"
                '''
            }
        }
        stage('Test Screen') {
            steps {
                bat '''
                "C:\Users\nyyif\AppData\Local\Programs\Python\Python39\python.exe" -c "import screen; screen.welcome(); print('Screen test passed')"
                '''
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