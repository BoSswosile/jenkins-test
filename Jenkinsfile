pipeline {
    agent none
    stages {
        stage('Checkout code') {
            agent any
            steps {
                git branch 'source', url: 'https://github.com/BoSswosile/jenkins-test.git'   
            }
            
        }
        stage('Build Backend') {
            agent {
                label 'docker-agent-python'
            }
            steps {
                sh 'pip install -r requirements.txt'
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