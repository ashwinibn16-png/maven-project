
pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out Maven project'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Maven project'
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Maven tests'
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                echo 'Packaging Maven project'
                bat 'mvn package'
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESSFUL!'
        }

        failure {
            echo 'BUILD FAILED!'
        }
    }
}
