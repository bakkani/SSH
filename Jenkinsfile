timestamps {
    node ('Built-IN'){

   // environment {
     //   AWS_CREDENTIALS = credentials('dev')
  //  }
   environment {
        AWS_ACCESS_KEY_ID     = credentials('aws_access_key_id')
        AWS_SECRET_ACCESS_KEY = credentials('aws_secret_access_key')
    }
  

        stage('Copy Files to EC2') {
            script {
               

            // Define your EC2 instance details
            def ec2Host = '54.80.212.119'
            def ec2User = 'ubuntu'
            def localFilePath = 'test.txt'
            // echo "FILE Parameter Value: ${localFilePath}"
            def remoteDirectory = '/tmp/dir/'
            def password = 'Pavankalyanbakkani@123'

            // Copy files using scp
           // sh "scp ${password} ${localFilePath} ${ec2User}@${ec2Host}:${remoteDirectory}"
            sh '''
ssh -i /home/ubuntu/devient_key.pem ${ec2User}@${ec2Host}
'''

        }
    }
}
}

