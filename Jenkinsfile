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
    stage('test') {
      steps {
        sh 'mvn test'
        junit(testResults: '**/target/*.xml', allowEmptyResults: true)
      }
    }
  }
}