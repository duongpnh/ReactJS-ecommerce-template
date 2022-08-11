pipeline {
    agent none
    environment {
        DOCKER_IMG = 'ecommerce/template1'
    }
    stages {
        stage('Test') { 
            agent {
                docker {
                    image 'node:12'
                    args '-u 0:0'
                }
            }
            steps {
                sh 'npm install'
            }
        }
        // stage('Build') { 
        //     steps {
        //         sh 'yarn'
        //     }
        // }
        // stage('Deploy') { 
        //     steps {
        //         sh 'yarn'
        //     }
        // }
    }
    post {
        success {
            echo "SUCCESS"
        }
        failure {
            echo 'FAILED'
        }
    }
}