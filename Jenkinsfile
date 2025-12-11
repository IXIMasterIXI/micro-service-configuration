pipeline {
    agent any
    stages {
        stage('Kill services') { 
            steps {
                sh 'pkill -f java' 
            }
        }
        stage('Test') { 
            steps {
                sh 'mvn test' 
            }
        }
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Deploy'){
            steps{
                sh 'BUILD_ID=dontKillMe java -jar target/config-service-0.0.1-SNAPSHOT.jar &'
            }
        }
    }
}
