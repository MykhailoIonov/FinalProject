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
        stages {
        stage('upload') {
           steps {
              script { 
                 def server = Artifactory.server 'node_main'
                 def uploadSpec = """{
                    "files": [{
                       "pattern": "/home/ubuntu/test/spring-petclinic/target/*jar",
                       "target": "/home/ubuntu"
                    }]
                 }"""

                 server.upload(uploadSpec) 
               }
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
