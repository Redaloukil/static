pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-1' , credentials:'aws-static') {
                    sh 'echo "Uploading content with AWS creds"'
                    s3Upload(file:'index.html', bucket:'jenkinsreda', path:'/')
                }   
            }
        }
    }
}