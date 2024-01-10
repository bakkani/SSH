pipeline {
    agent any

   parameters {
  base64File 'FILE'
}


    stages {
        stage('Display Base64 Decoded Content') {
            steps {
                script {
                    echo "Base64-encoded content:"
                    echo "$FILE"
                }

                script {
                    echo "Decoded content using environment variable:"
                    sh 'echo $FILE | base64 -d'
                }
            }
        }
    }
}
