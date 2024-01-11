timestamps {
    agent built-in

   // environment {
     //   AWS_CREDENTIALS = credentials('dev')
  //  }

  parameters {
            choice(name: 'ENVIRONMENT', choices: ['dev', 'uat', 'prod'], description: 'Select environment')
        // file(name: 'uploadedFile', description: 'Select a file to upload')
        }

        stage('Copy Files to EC2') {
            script {
               // def FILE = "${params.uploadedFile}"
 
                // Print the file path for debugging
               // echo "Uploaded file: ${FILE}"
               // echo "Parameters: ${params}"
              //  echo "ENVIRONMENT: ${params.ENVIRONMENT}"
              //  echo "Uploaded file: ${params.uploadedFile}"
                  // Print the file path for debugging
               // echo "Uploaded file: ${FILE}"
//def uploadedFile = params.uploadedFile
             //   if (uploadedFile == null) {
                 //   error 'Uploaded file parameter is null. Check if the file is being properly uploaded.'
              //  }

            // Change directory and set AWS profile and region based on the environment
            sh '''
            

                    
                if [ "$ENVIRONMENT" == "dev" ]; then
                    export AWS_PROFILE=dev
                    export AWS_DEFAULT_REGION=us-east-1
                elif [ "$ENVIRONMENT" == "uat" ]; then
                    export AWS_PROFILE=uat
                    export AWS_DEFAULT_REGION=us-east-1
                elif [ "$ENVIRONMENT" == "prod" ]; then
                    export AWS_PROFILE=prod
                    export AWS_DEFAULT_REGION=${AWS_REGION}
                else
                    echo "Invalid environment specified"
                    exit 1
                fi
            '''

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

