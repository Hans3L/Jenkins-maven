#!groovy

node {
    try {
        stages {
            stage('Build') {
                steps {
                    sh 'make'
                }
            }
            stage('Test') {
                steps {
                    sh 'make'
                    sh 'time'
                }

            }
            stage('Deploy') {
                sh 'make publish'
                sh 'time'
            }

            stage 'Publish results'
            slackSend color: "good", message: "Build successful: `${env.JOB_NAME}#${env.BUILD_NUMBER}` <${env.BUILD_URL}|Open in Jenkins>"

        }

    } catch (err) {
        slackSend color: "danger", message: "Build failed :face_with_head_bandage: \n`${env.JOB_NAME}#${env.BUILD_NUMBER}` <${env.BUILD_URL}|Open in Jenkins>"


    }


}
