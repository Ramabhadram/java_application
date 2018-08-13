pipeline {
   agent { label 'master' }

    stages {
        
        stage('Checkout') {
            steps {
        checkout scm
            }
    }
        stage('Build') {
            steps {
                echo 'Building..'
                 sh 'mvn package'
            }
        }
       
        
        
        stage('Deploy') {
            steps {
                sh 'sudo apt update -y'
                
            }
        }
    }
}
