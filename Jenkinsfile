pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the repository'
            }
        }
        stage('Build') {
            steps {
                
                echo 'Building the project'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the project'
            }
        }
    }
    post {
        always {
            echo 'Pipeline finished!'
        }
    }
}
