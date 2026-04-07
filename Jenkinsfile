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
                bat 'set KUBECONFIG=C:\\Users\\Admin\\.kube\\config && kubectl apply -f deployment.yaml'
                bat 'set KUBECONFIG=C:\\Users\\Admin\\.kube\\config && kubectl apply -f service.yaml'
            }
        }
    }
}
