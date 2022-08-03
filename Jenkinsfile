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
                echo "${env.BUILD_NUMBER}"
                echo "${env.BUILD_URL}"
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
                script {
                    if (env.BRANCH_NAME == "master" || env.BRANCH_NAME == "develop")
                        echo 'Test'
                    }
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
        stage('Prod Approval') {
            steps {
                script {
                    if (env.BRANCH_NAME == "master") {
                    input('Proceed for Prod Deployment?')
                    }
                }
            }
        }
        stage('Deploy to Prod') {
            steps {
                script {
                    if (env.BRANCH_NAME == "master") {
                echo 'Prod'
                    }
            }
        }
    }
}