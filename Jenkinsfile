def dockerhub = "zayyanabdillah/jenkins"
def image_name = "${dockerhub}:${BRANCH_NAME}"
def builder

pipeline {
    agent any

    stages {
        stage ("installing dependencies") {
            steps {
                nodejs("node14") {
                    sh 'npm install'
                }
            }
        }
        stage ("building docker image") {
            steps {
                script {
                    builder = docker.build("${image_name}")
                }
            }
        }
    }
}