@Library('jenkins-shared-library') _
pipeline {

    agent { label 'slave_node1' }

    tools {
        maven 'maven3.9'
    }

    stages {
        stage('Checkout') {
            steps {
                script {
                    scmCheckout()
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    build()
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    test()
                }
            }
        }
    }
}