pipeline {
    agent none
    stages {
        stage('Checkout code') {
            agent any
            steps {
                git url: 'https://github.com/BoSswosile/jenkins-test.git', branch: 'source'
            }
        }
        
        stage('Build Backend') {
            agent {
                label 'docker-agent-python'
            }
            steps {
                sh 'pip install -r back/requirements.txt'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing....'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}