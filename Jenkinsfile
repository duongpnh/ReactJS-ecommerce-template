pipeline {
    agent none
    environment {
        DOCKER_IMG = 'ecommerce/template1'
    }
    stages {
        stage('Test') { 
            agent {
                docker {
                    image: 'yarnpkg/node-yarn'
                    args '-u 0:0'
                }
            }
            steps {
                sh 'yarn'
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