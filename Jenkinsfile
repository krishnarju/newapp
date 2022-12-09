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
               sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
