pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/your-username/node-app.git'
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo "No tests yet"
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t node-app .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker run -d -p 3000:3000 node-app'
            }
        }
    }
}
