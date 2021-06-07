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
                sh 'cd spring-petclinic'
                sh 'ls -la'
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
