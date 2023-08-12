pipeline {
    agent {
        node {
            label 'maven'
        }
    }
    stages {
        stage('git checkout') { 
            steps {
                git branch: "master", url: "https://github.com/chowdarybvsn/tweet-trend-mine.git"
            }
        }
        stage('mvn install') {
           steps {
             sh 'mvn clean deploy'
          }
       }
        stage('SonarQube analysis') {
        environment {
             scannerHome = tool 'Mysonar'
        }
        steps{
         withSonarQubeEnv('Mysonar')
             sh "${scannerHome}/bin/sonar-scanner"
            }
        }
    }
}
  