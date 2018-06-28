pipeline {
  agent {
    docker {
      image 'maven:3.5.4-jdk-8-alpine'
      args '-v /root/.m2:/root/.m2'
    }

  }
  stages {
    stage('build') {
      steps {
        sh 'echo "Hello Welcome To The Cloud"'
        sh 'mvn --version'
        sh 'mvn install'
      }
    }
  }
  environment {
    DOCKER_HOST = 'tcp://192.168.56.100:2376'
    DOCKER_TLS_VERIFY = '1'
  }
}