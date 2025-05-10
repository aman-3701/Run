
pipeline {
    agent any
    stages {
        stage('Docker') {
            steps{
            sh 'docker login  -u amandevops8080 -p iAdmin@123'
        }
            steps{
                sh 'docker build -t amandevops8080/test .'
        }
        
    }
    }
}
