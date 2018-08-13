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
                sh 'sudo apt install tomcat8 -y'
                sh 'sudo apt install tomcat8-admin -y'
                sh 'sudo apt install tomcat8-user -y'
                sh 'sudo cp /var/lib/jenkins/workspace/Java_applicaion_docker/target/grants.war /var/lib/tomcat8/webapps/'
                sh 'sudo cp /var/lib/jenkins/workspace/Java_applicaion_docker/tomcat-users.xml /etc/tomcat8/'
                sh 'sudo service tomcat8 restart'

            }
        }
    }
}
