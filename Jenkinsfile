pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Build started"
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo "Testing..."
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t nano-app .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker run -d -p 3000:3000 nano-app || true'
            }
        }
    }
}
