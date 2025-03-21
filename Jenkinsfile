pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'make -C main' 
      }
    }
    stage('Test') {
      steps {
        sh './main/hello_exec' // Runs the compiled hello.cpp program
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
  }
  
  post {
    failure {
      echo 'Pipeline failed!' 
    }
  }
}
