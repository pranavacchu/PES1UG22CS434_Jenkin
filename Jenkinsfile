pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'make -C main' // This will run the Makefile in the 'main' folder
      }
    }
    stage('Test') {
      steps {
        sh './main/hello_exec' // Runs the compiled hello.cpp program
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...' // Placeholder for actual deployment steps
      }
    }
  }
  
  post {
    failure {
      echo 'Pipeline failed!' // If the pipeline fails, this message will be printed
    }
  }
}
