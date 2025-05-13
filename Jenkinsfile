pipeline {
    agent any  // Runs the pipeline on any available agent (node)

    stages {
        stage('Build') {
            steps {
                echo 'Building the application'
                // Add build commands here (example for Node.js):
                sh 'npm install'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running tests'
                // Add testing commands (example for Node.js):
                sh 'npm test'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying the application'
                // Add deployment commands here (example):
                sh './deploy.sh'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed, check the logs.'
        }
    }
}
