pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Abhaysoni16/HTML'
                
            }
        }
        stage('Build'){
            steps{
                sh 'docker build -t test .'
            }
            
            
        }
        stage("deployment "){
            steps{
                
                sh 'docker tag test Abhaysoni16/test:1'
                sh 'docker login -u Abhaysoni16 -p ''
                sh'docker push Abhaysoni16/test:1 '
                sh 'docker compose down && docker compose up -d'
            }
            
        }
    }
}
