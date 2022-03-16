node {


    stage('Clone repository') {
        echo "Checking out..."
        checkout scm
    }
    stage('Test') {
        
        echo 'Testing..'
        
    }
    stage('Build') {
        echo "Building..."
        docker.withRegistry('https://298621573365.dkr.ecr.us-east-1.amazonaws.com/bca', 'ecr:us-east-1:aws') {
            def image = docker.build("bca:${env.BUILD_TAG}", ".")
            image.push('latest')
        }
    }
    stage('Deploy') {
        echo 'Deploying....'
        sh 'aws ecs update-service --cluster bca-cluster --service bca-ecs-service --force-new-deployment'
    }
}