pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/your-repo.git', branch: 'main'
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
