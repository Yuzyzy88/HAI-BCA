node {

    environment {
        AWS = credentials('aws') 
    }
    stage('Clone repository') {
        echo "Checking out..."
        checkout scm
    }
    stage('Test') {
        
        echo 'Testing..'
        
    }
    stage('Build') {
        echo "Building..."
        def newApp = docker.build("bca_nginx:${env.BUILD_TAG}", ".")

        echo "Username is $AWS_USR"
        echo "Username is $AWS_PSW"
    }
    stage('Deploy') {
        
        echo 'Deploying....'
        
    }
}