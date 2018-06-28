pipeline {
  agent {
    docker {
      image 'maven:3.5.4-jdk-8-alpine'
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
}