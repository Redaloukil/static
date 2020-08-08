pipeline {
    agent any
    stages {
        stage('Hello'){
            sh "echo hello world"
            sh "echo $AWS_CREDENTIALS"
        }

        // stage('Upload to AWS') {
        //     steps {
        //         withAWS(region:'us-east-1' , credentials:"aws-static") {
        //            sh "works"
        //         }   
        //     }
        // }
    }
}