pipeline {
  agent any 
    stages {
        stage('Build') {
            steps {
              script {
              sh 'g++ --version'
                sh 'g++ task5.cpp'
                sh
                echo 'Build Stage Successful'
              }
                
            }
        }

        stage('Test') {
            steps {
              script {
                sh './task5'
                echo 'Test Stage Successful'
              }
                
                
            }
        }

        stage('Deploy') {
            steps {
              script {
              sh 'mvn deploy'
                echo 'Deployment Successful'
              }
                
            }
        }
    }

    post {

        failure {
            echo 'Pipeline failed'
        }
    }
}
