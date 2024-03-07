pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Assuming 'PES2UG21CS422-1' is a predefined job in Jenkins that you want to trigger
                build 'PES2UG21CS422-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                // Introducing an intentional mistake by using a non-existent command
                sh './invalid_command'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
