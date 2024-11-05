pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                
                git 'https://github.com/iqbalalisha/Dockerized-app.git'
                
                sh 'npm install' 
            }
        }
        stage('SonarQube Analysis') {
            steps {
                 
                script {
                    withSonarQubeEnv('sonarserver') {  
                        sh 'sonar-scanner'
                    }
                }
            }
        }
        stage('Run Docker Container') {
    steps {
        script {
            sh 'docker build -t my-frontend-app .'
            sh 'docker run -d -p 85:80 my-frontend-app'
        }
    }
}

    }
}
