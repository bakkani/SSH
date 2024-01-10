timestamps {
    node('built-in') {
        stage('CleanWorkspace') {
            cleanWs()
        }
       parameters {
       base64File 'FILE'
      }
  
    stage('Example') {
      
        withFileParameter('FILE') {
          sh 'cat $FILE'
        }
      
    
  }
}
}
