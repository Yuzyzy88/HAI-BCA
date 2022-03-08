node {


    stage('Clone repository') {
        echo "Checking out..."
        checkout scm
    }
    stage('Build') {
        echo "Building..."
        def newApp = docker.build "bca_nginx:${env.BUILD_TAG}"  
    }
    stage('Test') {
        
        echo 'Testing..'
        
    }
    stage('Deploy') {
        
        echo 'Deploying....'
        
    }
}