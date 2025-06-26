pipeline {
    agent any

    environment {
        KUBECONFIG = "/var/jenkins_home/.kube/config"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Deploy Nginx to Kubernetes') {
            steps {
                sh 'kubectl apply -f nginx-deployment.yaml'
            }
        }
    }
}
