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
                sh 'ls -la .ssh/'
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
