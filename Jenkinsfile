pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS016-1'
                sh 'g++ new.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './new'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'
        }
    }
}
