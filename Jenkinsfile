def dockerhub = "zayyanabdillah/jenkins"
def image_name = "${dockerhub}:${BRANCH_NAME}"
def builder

pipeline {
    agent any

    stages {
        stage(insstalling dependencies) {
            steps {
                nodejs("node14") {
                    sh "npm install"
                }
            }
        }
    }
}