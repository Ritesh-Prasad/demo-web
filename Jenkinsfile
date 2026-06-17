pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git ''
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devopsbyritesh:v1 .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8080:80 --name devops-site devopsbyritesh:v1 || true'
            }
        }
    }
}
