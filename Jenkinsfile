pipeline {
  agent any
  environment {
	TEST = 'test1'
  }
  stages {
    stage('Hello World') {
      steps {
        echo "Hello World"
        echo "${TEST} $TEST"
        sh 'printenv'
        sh '''
          echo "Multiline shell steps works too"
          ls -lah
        '''
      }
    }
  }
}

