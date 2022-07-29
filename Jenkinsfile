pipeline {
  agent any 

  tools {
    maven 'mvn'
  }

  stages {

    stage('Build') {
      steps {
        echo 'Build ' + env.BRANCH_NAME
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