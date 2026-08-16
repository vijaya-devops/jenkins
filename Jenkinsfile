pipeline {
    agent {
        node {
            label 'ROBOSHOP'
        }
        environment {
           COURSE = 'Jenkins'
    }
    // build
    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building..'
                    echo "Course name is ${COURSE}"
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'Testing..'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying....'
                }
            }
        }
    }

    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success {
            echo 'I will say Hello only if successful'
        }
        failure {
            echo 'I will say Hello only if failed'
        }
    }
}