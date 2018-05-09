pipeline {
  agent any
  stages {
    stage('step 1') {
      parallel {
        stage('test') {
          steps {
            slackSend 'test'
          }
        }
        stage('echo') {
          steps {
            sh 'echo "Hello world!";'
          }
        }
      }
    }
    stage('') {
      steps {
        dir(path: '/home/deploy/playbooks') {
          sh 'echo "Done!";'
        }

      }
    }
  }
}