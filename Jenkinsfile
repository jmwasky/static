pipeline {
  agent any
  environment {
	TEST = 'test1'
  }
  env.TEST2 = 'tet2'
  stages {
    stage('Hello World') {
      steps {
        echo "Hello World"
        echo "${env.TEST2}"
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

