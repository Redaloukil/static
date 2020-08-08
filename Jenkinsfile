pipeline {
    agent any
    stages {
        stage('Hello'){
            step {
                sh "echo hello world"
                sh "echo $AWS_SECRET_ACCESS_KEY"
                sh "echo $AWS_DEFAULT_REGION"
                sh "echo $AKIA5GV6U7ZYFN4BVP6N"
 
            }
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