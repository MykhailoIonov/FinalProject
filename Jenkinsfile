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
                sh '''
                cd spring_petclinic
                sudo chmod +x mvnw
                sudo ./mvnw package
                '''
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
