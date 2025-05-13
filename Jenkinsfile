pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application'
                bat 'echo Hello from Windows Build'  // <-- use `bat` instead of `sh`
            }
        }
        stage('Test') {
            steps {
                echo 'Testing the application'
                bat 'echo Running tests...'          // Replace `sh` with `bat`
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application'
                bat 'echo Deploy completed'          // Windows-compatible deploy command
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed, check the logs.'
        }
    }
}
