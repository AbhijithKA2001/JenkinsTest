pipeline {
    agent any
    tools {
        nodejs 'Node'
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Linting') {
            steps {
                sh 'npm run lint'
            }
        }
        stage('Type Checking') {
            steps {
                sh 'npm run flow'
            }
        }
        stage('Unit Tests') {
            steps {
                sh 'npm run test'
            }
        }
    }
}
