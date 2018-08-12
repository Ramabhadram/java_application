pipeline {
    
agent any

    stages {
        stage('Build Code') {
            steps {
                echo 'Building..'
                sh 'mvn package'
                  }
                       }
        
           }
        
        
        
        stage('Build Docker Image') {
            steps {
                echo 'Building Docker..'
                sh 'sudo docker build -t ramdocker/javaapp .'
                sh 'sudo docker run -p 8090:8080 -d ramdocker/javaapp'
                    }
                }
                
}
