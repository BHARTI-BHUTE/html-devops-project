pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Downloading latest code from GitHub'
            }
        }

        stage('Verify Project') {
            steps {
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t html-app:v1 .'
            }
        }

        stage('Verify Docker Image') {
            steps {
                sh 'docker images'
            }
        }

        stage('Pipeline Completed') {
            steps {
                echo 'Docker Image Created Successfully'
            }
        }

    }

}
