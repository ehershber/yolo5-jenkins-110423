pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                aws ecr get-login-password --region eu-west-3 | docker login --username AWS --password-stdin 700935310038.dkr.ecr.eu-west-3.amazonaws.com
                docker build -t ehershber-yolo5 .
                docker tag ehershber-yolo5:latest 700935310038.dkr.ecr.eu-west-3.amazonaws.com/ehershber-yolo5:latest
                docker push 700935310038.dkr.ecr.eu-west-3.amazonaws.com/ehershber-yolo5:latest

                '''
            }
        }
    }
}