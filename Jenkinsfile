pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS547-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                eccho 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
