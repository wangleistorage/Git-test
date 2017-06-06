pipeline {
  agent any
  stages {
    stage('mkdir /tmp/111') {
      steps {
        sh 'mkdir -p /tmp/111'
      }
    }
    stage('mkdir /tmp/222') {
      steps {
        sh 'mkdir -p /tmp/222'
      }
    }
    stage('Build a wanglei-test') {
      steps {
        build(job: 'wanglei-test', propagate: true, quietPeriod: 10, wait: true)
        sh 'echo 66666'
      }
    }
  }
}