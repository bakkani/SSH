timestamps {
    node('built-in') {
        stage('CleanWorkspace') {
            cleanWs()
        }
       parameters {
       base64File 'THEFILE'
      }
  
    stage('Example') {
      
        withFileParameter('THEFILE') {
          sh 'cat $THEFILE'
        }
      
    
  }
}
}
