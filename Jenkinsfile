pipeline {
    agent any

    stages {
        stage("Checkout business repo") {
            steps {
                git (
                    branch: 'master', 
                    url: 'https://github.com/Mangushaa/jenkins-project-test.git'
                )
            }
        }
        stage('Build') {
            steps {
                sh 'mvnw package -DskipTests'
            }
        }
        stage('Test') {
            steps {
                sh 'mvnw test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}