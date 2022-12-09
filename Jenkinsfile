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
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
