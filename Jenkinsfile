pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'mvn clean'
            }
        }
        /*stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn package'
            }
        }*/
    }
}
