pipeline {
    agent {
        node {
            label 'node'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'ls -la'
                sh 'ls -la spring-petclinic/'
            }
        }
        stage('Test') {
            steps {
                sh 'cd spring-petclinic;
                    ls -la' 
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
