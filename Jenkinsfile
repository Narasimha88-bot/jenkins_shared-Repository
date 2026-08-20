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
        stage('Deploy to the Artifactory') {
            steps {
                script {
                    deploy()
                }
            }
        }
        stage ('Download from the artifactory') {
            steps {
                script {
                    download()
                }
            }
        }
    }
}
