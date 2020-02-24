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
    stage('Cope file to /var/jenkins_home/shsnc-worksplace') {
      steps {
        sh 'cp index.html /var/jenkins_home/shsnc-worksplace'
      }
    }  
  }  
}
