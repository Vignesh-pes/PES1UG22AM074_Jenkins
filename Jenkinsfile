pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'g++ -o PES1UG22AM074 main.cpp' // Compile the C++ file
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './Nofile' // Execute compiled C++ program
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh 'echo "Application deployed successfully!"'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline completed successfully.'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
