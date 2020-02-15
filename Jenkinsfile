pipeline {
  agent any
  stages {
    stage('Hello World') {
      steps {
        sh 'echo "Hello World"'
        sh '''
          echo "Multiline shell steps works too"
          ls -lah
        '''
      }
    }
	stage('Tidy lint HTML.') {
      steps {
        sh 'tidy -q -e *.html'
      }
    }
    stage('Upload to AWS 2') {
      steps {
        withAWS(credentials:'aws-static') {
            s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:'jinkens-proj03')
        }
      }
    }
  }
}
