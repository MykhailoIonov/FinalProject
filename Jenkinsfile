pipeline {
    agent {
        node {
            label 'node_main'
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
                sh 'sudo chmod +x spring_petclinic/mvnw'
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
