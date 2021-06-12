pipeline {
    agent {
        node {
            label 'node'
        }
    }
    stages {
        stage('Checkout code'){
            steps {
                 checkout scm
            }
       }
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'ls -la'
                sh 'sudo ./spring_petclinic/mvnw package'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
