pipeline {
    agent any

    triggers {
        // Poll SCM every 5 minutes
        pollSCM('H/1 * * * *')





    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the project using Maven'
                // e.g., sh 'mvn clean package' or bat 'mvn clean package' on Windows
            }
        }

        stage('Unit and Integration Tests') {

            
            steps {
                echo 'Running unit and integration tests with JUnit'
                // e.g., sh 'mvn test' or relevant test command
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Running code analysis with SonarQube scanner'
                // e.g., sh 'sonar-scanner' or call SonarQube Jenkins plugin
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Performing security scan with OWASP Dependency-Check'
                // e.g., sh 'dependency-check.sh --project my-project --scan .' 
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying app to AWS EC2 staging environment'
                // Use ssh, Ansible, or AWS CLI commands here
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging environment'
                // e.g., sh 'mvn verify -Pintegration-tests' or run Postman/Newman tests
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying app to production environment'
                // Similar to staging deploy but for production servers
            }
        }
    }
}
