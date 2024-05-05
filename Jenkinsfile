pipeline {
    agent any
    stages {
        stage ('test') {
            steps {
                sh 'docker ps -a'
            }
        }
        stage ('Run Docker Compose') {
            steps {
                sh 'docker-compose up -d --build'
            }
        }
    }

    post{
          success{
              script{
                    slackSend channel: 'filrougeg3', message: 'Le buil est effectuer avec success'
              }
          }
        failure{
              script{
                    slackSend channel: 'filrougeg3', message: 'Erreur :Echec du buil!'
              }
          }
        }
  
}




