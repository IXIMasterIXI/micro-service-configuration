pipeline {
    agent any
    stages {
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
    }
}
