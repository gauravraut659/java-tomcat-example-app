pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                bat 'mvn package'
                sshagent(['tomcat1']) {
                     bat """
                     ssh -o StrictHostKeyChecking=no **/*.war windows@localhost:9090:/E:\Gaurav_Raut_Data\DevOps_Bootcamp\tomcat\apache-tomcat-9.0.34-windows-x64\apache-tomcat-9.0.34\webapps
                     """
                        }
            }
        }
    }
}
