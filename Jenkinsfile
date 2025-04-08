pipeline {
    agent any
    environment { IMAGE = "farahsalmi02996/greeting_app:latest" }
    stages {
        stage('Review')    { 
            steps { 
                sh 'docker run -d -p 8080:80 --rm --name review $IMAGE' 
            } 
        }
        stage('Staging')   { 
            steps { sh 'docker run -d -p 8081:80 --rm --name staging $IMAGE' 
            } 
        }
        stage('Production'){ 
            steps { sh 'docker run -d -p 80:80 --rm --name production $IMAGE' 
            } 
        }
    }
}