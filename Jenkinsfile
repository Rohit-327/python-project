pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t devops-app:v1 .'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
               bat 'kubectl apply -f deployment.yaml --validate=false'
               bat 'kubectl apply -f service.yaml --validate=false'
            }
        }
    }
}
