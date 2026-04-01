pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'echo Build stage'
            }
        }

        stage('Test') {
            steps {
                bat 'echo Test stage'
            }
        }

        stage('Docker Build') {
            steps {
                bat 'docker build -t build1-site .'
            }
        }

        stage('Docker Run') {
            steps {
                bat 'docker rm -f build1-container'
                bat 'docker run -d -p 8085:80 --name build1-container build1-site'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo Deploy completed'
            }
        }
    }
}