pipeline {
    agent any

    stages {
        stage('Clone repository') {
            /* Let's make sure we have the repository cloned to our workspace */
            echo "Checking out..."
            checkout scm
        }
        stage('Build') {
            steps {
                def myEnv = docker.build 'my-environment:snapshot'
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