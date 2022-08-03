pipeline {
    agent any
    tools {
        maven 'Maven'
            }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Code Quality') {
            steps {
                echo 'Quality....'
            }
        }
        stage('Deploy to Dev') {
            steps {
                echo 'Dev....'
            }
        }
        stage('Deploy to Test') {
            steps {
                echo 'Test'
            }
        }
        stage('Deploy to UAT') {
            steps {
                echo 'UAT'
            }
        }
        stage('Deploy to Pre_prod') {
            steps {
                echo 'Stagging'
            }
        }
        stage('Deploy to Prod') {
            steps {
                echo 'Prod'
            }
        }
    }
}