pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
               git branch: 'main', credentialsId: 'krish', url: 'https://github.com/krishnarju/newapp.git'
            }
        }
        stage('build') {
            steps {
                mvn clean package -DskipTests
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
