pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
                git clone "https://github.com/krishnarju/newapp.git"
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
