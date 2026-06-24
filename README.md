pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // This step automatically checks out your GitHub code
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building your project...'
                // Add your build commands here (e.g., sh 'npm install' or sh 'mvn clean install')
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your testing commands here (e.g., sh 'npm test')
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying project...'
            }
        }
    }
}
