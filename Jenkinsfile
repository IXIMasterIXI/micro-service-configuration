pipeline {
  
  agent any
  
   stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/IXIMasterIXI/micro-service-configuration.git'
            }
        }
        //stage('Build') {
          //  steps {
            //    sh 'mvn clean install' 
           // }
        //}
        stage('Test') {
            steps {
                sh './mvn test'
            }
        }
        stage('Package') {
            steps {
                sh './mvn package'
            }
        }
        stage('Deploy') {
            steps {
                sh './ls'
            }
        }
    }
    post {
        success {
            echo 'Build and Deploy succeeded!'
        }
        failure {
            echo 'Build or Deploy failed!'
        }
    }
}
