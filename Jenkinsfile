@Library('Practice_Shared_Librar') _
pipeline {

    agent { label 'slave_node' }

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
        stage('Deploy and download from the artifactory') {
            steps {
                script {
                    deploy_download_copytotomcat()
                }
            }
        }
    }
}
