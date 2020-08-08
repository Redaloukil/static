pipeline {
    agent any
    stages {
        stage('Test'){
            steps {
                
                sh "echo hello world"
                sh "echo $AWS_SECRET_ACCESS_KEY"
                sh "echo $AWS_DEFAULT_REGION"
                sh "echo $AWS_ACCESS_KEY_ID"
                   
            }
        }
        stage('Upload aws') {
            steps {
                withAWS(region:'us-east-1' , credentials:"aws-static") {
                    sh 'echo "Uploading content with AWS creds"'
                    s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkinsreda', path:'/'){
                        sh "echo works"
                    }
                }
            }
        }
    }
}