pipeline {
    agent {
        node {
            label 'ROBOSHOP'
        }
    }
        environment {
           COURSE = 'Jenkins'
        }
    options {
       
        disableConcurrentBuilds()
        timeout(time: 1, unit: 'MINUTES')
    }
     parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    // build
    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building..'
                    echo "Course name is ${COURSE}"
                    echo "Hello ${params.PERSON}"
                    echo "Biography: ${params.BIOGRAPHY}"
                    echo "Toggle: ${params.TOGGLE}"
                    echo "Choice: ${params.CHOICE}"
                    echo "Password: ${params.PASSWORD}"
                    ------
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