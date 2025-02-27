pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git(url: 'https://github.com/slyw0w/MySoftware.git', branch: 'main')
            }
        }
        stage('Run Tests') {
            steps {
                echo "Running tests..."
                sh 'python3 -c "from button import click; click()"'
                sh 'python3 -c "from screen import welcome; welcome()"'
            }
        }
    }
}
