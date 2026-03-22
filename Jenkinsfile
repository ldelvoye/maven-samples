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

    stage('run') {
      steps {
        bat 'mvn verify'
      }
    }

  }
}
