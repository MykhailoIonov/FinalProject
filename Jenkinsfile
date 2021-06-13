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
                stash name: "artifact", includes: "spring_petclinic/target/*.jar"
            }
        }
        stage ('unstash') {
            node { label  'node_prod' }
                 steps {
                    script {
                        unstash name: "artifact"  // runs in $WORKSPACE, creates $WORKSPACE/myfile.txt
                    }
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
