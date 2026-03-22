pipeline {
  agent any
  tools { 
      maven 'DHT_MVN' 
      jdk 'DHT_SENSE' 
  }
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/ldelvoye/maven-samples.git', branch: 'master')
      }
    }

    stage('mvn clean') {
      steps {
        bat 'mvn clean'
      }
    }

    stage('mvn test') {
      steps {
        bat 'mvn test'
      }
    }

    stage('mvn verify') {
      steps {
        bat 'mvn verify'
      }
    }

  }
}
