pipeline {

agent any

    stages{

            stage('clean the code ')
            {
                steps{
                    echo 'mvn clean'
                }
            }

            stage('unit testing')
            {
                steps{
                    echo 'mvn test'
                }
            }
            stage('deploy to tomcat')
            {
                steps{
                    echo 'mvn package'
                    
                }
            }
    }
}
