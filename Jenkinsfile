pipeline {
  agent any 

  stages {

    stage('Checkout') {
      steps {
        checkout scm
      }
    }

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