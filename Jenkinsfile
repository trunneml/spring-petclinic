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
    DOCKER_TLS_VERIFY = '0'
    DOCKER_HOST = 'unix:///var/run/docker.sock'
  }
}