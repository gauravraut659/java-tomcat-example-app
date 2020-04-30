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
                     ssh -o StrictHostKeyChecking=no **/*.war -l cloudbees 192.168.1.106 windows -a
                     """
                        }
            }
        }
    }
}
