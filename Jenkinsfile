pipeline {
    agent{
        node{
            label 'maven'
        }
    }
    stages{
        stage{
            step{
                git branch: "master", url: "https://github.com/chowdarybvsn/tweet-trend-mine.git"
            }
        }
       stage{
          step{
            sh 'mvn clean deploy'
          }
       }
    }
}
