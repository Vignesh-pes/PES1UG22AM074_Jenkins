pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'g++ -o hello_exec hello.cpp' // Compile the C++ file
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './hello_exec' // Execute compiled C++ program
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
