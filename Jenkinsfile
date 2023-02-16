pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ main/hello.cpp -o hello_exec'
            }
        }
        stage('Test') {
            steps {
                sh './hello_exec'
            }
        }
      stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post{
      failure{
          echo 'pipeline failed'
      }
    }
}


