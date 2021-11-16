pipeline {
    agent {label 'docker-label'}
    stages {
        stage('Build image') {
            steps {
                echo 'Starting to build docker image'
                git 'https://github.com/qfitsolutions/docker.git'
                script {
                    def customImage = docker.build("web:${env.BUILD_ID}")
                    customImage.push()
                }
            }
        }
    }
}
