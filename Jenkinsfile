timestamps {
    node('NEW_DSOD_Api_buildagent') {
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
