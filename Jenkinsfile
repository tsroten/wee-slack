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
    stage('test') {
      steps {
        dir(path: '/home/deploy/playbooks')
      }
    }
    stage('echo') {
      steps {
        sh 'echo "Done!";'
      }
    }
  }
}