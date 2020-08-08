pipeline {
    agent any
    stages {
        stage('Linting HTML') {
            sh "tidy -q -e *.html"
        }
        stage('Upload aws') {
            steps {
                withAWS(region:'us-east-1' , credentials:"aws-static2") {
                    sh 'echo "Uploading content with AWS creds"'
                    s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html',bucket:'jenkinsreda')
                }
            }
        }
    }
}