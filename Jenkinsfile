pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                /* Let's make sure we have the repository cloned to our workspace */
                echo "Checking out..."
                checkout scm
            }
        }
        stage('Build') {
            steps {
                docker.build 'my-environment:snapshot'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}