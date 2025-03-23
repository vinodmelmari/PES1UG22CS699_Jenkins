pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG22CS699-1'
                sh 'g++ hello.cpp -o hello_exec'
            }
        }
        stage('Test') {
            steps {
                sh './hello'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
