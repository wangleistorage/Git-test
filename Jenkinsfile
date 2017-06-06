pipeline {
  agent any
  stages {
    stage('mkdir /tmp/111') {
      steps {
        sh '''echo mkdir 111

if [ -e /tmp/111 ]; then
    echo exists
else
    echo not exists
fi'''
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