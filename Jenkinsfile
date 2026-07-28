pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t flaskapp .'
            }
        }

        stage('Run Dev Container') {
            steps {
                bat 'docker run -d --name dev2-container -p 6000:6000 flaskapp'
            }
        }

        stage('Run Test Container') {
            steps {
                bat 'docker run -d --name test2-container -p 6001:6000 flaskapp'
            }
        }
    }
}
