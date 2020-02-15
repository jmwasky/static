pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        sh 'echo "Hello World"'
        sh '''
          echo "Multiline shell steps works too"
          ls -lah
        '''
      }
    }
    stage('Upload to AWS') {
      steps {
        withAWS(endpointUrl:'https://udacity.jenkins.prot3.isaac.com',credentials:'AKIAZP3K6ZDZAY3AZPC7') {
              s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:’index.html’, bucket:’jinkens-proj03’)
        }
      }
      
    }
    
  }
}
