pipeline {
    agent {
        node {
            label 'maven'
        }
    }
    stages {
        stage('git checkout') { 
            step {
                git branch: "master", url: "https://github.com/chowdarybvsn/tweet-trend-mine.git"
            }
        }
        stage('mvn install') {
           step {
             sh 'mvn clean deploy'
          }
       }
    }
}
