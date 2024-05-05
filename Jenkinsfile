pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                // Étape de déploiement avec Docker Compose
                bat 'docker-compose up -d'
            
            }
        }

    }
    post {
        success {
            // Envoyer une notification par e-mail si le déploiement est réussi
               emailext body: 'Votre application est déployée avec succés', subject: 'Le build s\'est bien effectue', to: 'mougaye1225@gmail.com'
        }
    }
}






