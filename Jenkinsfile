pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'Newrepo', credentialsId: 'PROD', poll: false, url: 'https://github.com/sasikumar3004/Newrepo'
                }
       }
        stage('Terraform Init') {
            steps {
                sh 'terraform init'
            }
}

            stage('Terraform Apply') {
            steps {
                sh 'terraform apply -- auto-approve'
            }
}
}
}
