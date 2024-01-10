pipeline {
    agent any

    environment {
        AWS_CREDENTIALS = credentials('dev')
    }

    stages {
        stage('Example') {
            steps {
                script {
                    // Use AWS credentials in your AWS CLI or SDK commands
                    sh "aws configure set aws_access_key_id "
                    sh "aws configure set aws_secret_access_key "
                    sh "aws s3 ls"  // Example AWS CLI command
                }
            }
        }
    }
}
