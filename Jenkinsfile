
pipeline {
    agent any
    stages {
        stage("Build Jar"){
            steps{
                sh 'mvn clean package'
            }

        }
        stage('Docker') {
            steps{
                
           withCredentials([usernamePassword(credentialsId: 'docker-hub-creds', usernameVariable: 'DOCKER_USER', passwordVariable: 'DOCKER_PASS')]) {
                    sh 'docker login -u $DOCKER_USER -p $DOCKER_PASS'
                }
            sh 'docker build -t amandevops8080/test1 .'
            sh 'docker push amandevops8080/test1'
            sh 'docker run --name myweb -d -p 8686:8686 amandevops8080/test1'
                
        }
          
        
    }
    }
}
