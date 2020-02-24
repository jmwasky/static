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
  }
  stages {
    stage('Cope file to /var/jenkins_home/shsnc-worksplace') {
      steps {
        sh 'echo "cope file:index.html"'
        cp index.html /var/jenkins_home/shsnc-worksplace
      }
    }
  }
}

