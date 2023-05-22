pipeline {
    agent any

    stages {
        stage('Unittest') {
            steps {
                sh '''
                pip install -r requirements.txt
                python3 -m pytest --junitxml results.xml tests
                '''
            }
        }
        stage('Lint') {
            steps {
                echo "linting"
            }
        }
        stage('Functional test') {
            steps {
                echo "testing"
            }
        }
    }
}