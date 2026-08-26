@Library('Practice_Shared_Library') _
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
    }
}
