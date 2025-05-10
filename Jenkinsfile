
pipeline {
    agent any
    stages {
        stage('Docker') {
            steps{
            sh 'docker login  -u amandevops8080 -p iAdmin@123'
            sh 'docker push amandevops8080/test'
            sh 'docker run --name 'myweb' -d -p 8686:8686 amandevops8080/test:latest'
                
        }
          
        
    }
    }
}
