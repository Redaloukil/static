pipeline {
    agent any
    stages {
        stage('Upload to AWS'){
            steps {
                sh "echo hello world"
                sh "echo $AWS_SECRET_ACCESS_KEY"
                sh "echo $AWS_DEFAULT_REGION"
                try {
                    sh "echo $AWS_ACCESS_KEY_ID"
                }catch{
                    sh "error while echo $AWS_ACCESS_KEY_ID"
                }
                
                withAWS(region:'us-east-1' , credentials:"aws-static") {
                   sh "works"
                }   
                
                
            }
        }
    }
}