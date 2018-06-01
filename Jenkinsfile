pipeline {
  agent {
    label 'master'
  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            ansiblePlaybook(credentialsId: 'root', inventory: '/root/gittes/hosts', playbook: '/root/gittes/mytest.yml')
          }
        }
        stage('') {
          steps {
            sh 'echo "hello"> /tmp/hello'
          }
        }
      }
    }
    stage('Test') {
      steps {
        sh 'echo ""> /tmp/test'
      }
    }
  }
}