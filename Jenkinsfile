pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-1' , username:'AKIA5GV6U7ZYFN4BVP6N' , password:'/4NbKzSpC/c4M3KxhNl+Fob9WT1NGMjJH0SCwHC0') {
                    sh 'echo "Uploading content with AWS creds"'
                    s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true,file:'index.html', bucket:'jenkinsreda', path:'/')
                }   
            }
        }
    }
}