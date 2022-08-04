pipeline {
    agent {
        image: 'yarnpkg/node-yarn'
        args '-u 0:0'
    }
    environment {
        DOCKER_IMG = 'ecommerce/template1'
    }
    stages {
        stage('Test') { 
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