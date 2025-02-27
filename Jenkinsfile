pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Change this URL to your MySoftware repository
                git url: 'https://github.com/slyw0w/MySoftware.git', branch: 'main'
            }
        }
        stage('Test Button') {
            steps {
                bat """
                python -c "try:
                    from button import click
                    click()
                    print('Button test passed')
                except Exception as e:
                    print(f'Button test failed: {e}')
                "
                """
            }
        }
        stage('Test Screen') {
            steps {
                bat """
                python -c "try:
                    from screen import welcome
                    welcome()
                    print('Screen test passed')
                except Exception as e:
                    print(f'Screen test failed: {e}')
                "
                """
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

