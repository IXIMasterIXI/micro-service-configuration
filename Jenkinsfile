//pipeline con las instrucciones para CI/DC de service configuration
pipeline {
    agent any
    stages {
        stage('Test') { 
            steps {
                sh 'mvn test' 
            }
        }
       // stage('package'){
        //    steps{
          //      sh 'mvn package'
            //}
        //}
        stage('Deploy'){
            steps{
                sh 'JENKINS_NODE_COOKIE=dontKillMe java -jar target/config-service-0.0.1-SNAPSHOT.jar &'
            }
        }
    }
}
