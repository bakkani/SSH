pipeline {
    agent any

    parameters {
        // Define a Base64 file parameter named FILE
        file(name: 'FILE', description: 'Base64-encoded file content')
    }

    stages {
        stage('Display Base64 Decoded Content') {
            steps {
                // Display the decoded content using an environment variable
                script {
                    echo "Decoded content using environment variable:"
                    sh 'echo $FILE | base64 -d'
                }

                // Display the decoded content using a temporary file
                script {
                    echo "Decoded content using a temporary file:"
                    withFileParameter('FILE') {
                        sh 'cat $FILE'
                    }
                }
            }
        }
    }
}
