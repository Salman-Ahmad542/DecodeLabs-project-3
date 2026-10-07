pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Project 3...'
                sh 'test -f index.html'
                sh 'test -f style.css'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing website files...'
                sh 'grep -q "CI/CD Pipeline Basics" index.html'
                echo 'All tests passed.'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying website...'
            }
        }
    }

    post {
        success {
            echo 'PROJECT 3 CI/CD PIPELINE SUCCESSFUL!'
        }

        failure {
            echo 'PROJECT 3 CI/CD PIPELINE FAILED!'
        }
    }
}
