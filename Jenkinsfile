pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Starting Build'
                sh 'make -C main'
                echo 'Build Completed'
            }
        }
        stage('Test') {
            steps {
                echo 'Starting Testing'
                sh '/var/jenkins_home/workspace/PES2UG20CS124-1/main/hello_exec'
                echo 'Test Completed'
            }
        }
        
    }
  post {
    failure {
      echo 'Pipeline Failed'
    }
  }
}
