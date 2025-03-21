pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22CS434-1 hello1.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS434-1'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying application...'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
