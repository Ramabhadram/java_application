pipeline {
   agent { label 'Ubuntu_VM' }

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
