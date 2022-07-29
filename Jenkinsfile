pipeline {
  agent any 

  tools {
    maven 'mvn'
  }

  stages {

    stage('Build') {
      steps {
        echo 'Build'
        sh 'mvn clean install'
      }
    }

    stage('Scanning') {
      steps {
        echo 'Scanning'
      }
    }
  }

}