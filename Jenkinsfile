pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'ant compile'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh 'ant test'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    sh 'ant deploy'
                }
            }
        }
    }

    post {
        success {
            echo 'Build and tests were successful!'
        }
        failure {
            echo 'Build or tests failed.'
        }
    }
}