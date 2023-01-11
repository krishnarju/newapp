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
        stage('SonarQube analysis') {
    def scannerHome = tool 'SonarScanner 4.0';
    withSonarQubeEnv('SonarQube Server') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
        
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
