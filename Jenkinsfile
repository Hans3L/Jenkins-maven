#!groovy

node {
    try {
        stages {
            stage('Build') {
                steps {
                    echo 'hola construye'
                }
            }
            stage('Test') {
                steps {
                    echo 'Prueba'
                }

            }
            stage('Deploy') {
                echo 'despliegue'
            }

            stage 'Publish results'
            slackSend color: "good", message: "Build successful: `${env.JOB_NAME}#${env.BUILD_NUMBER}` <${env.BUILD_URL}|Open in Jenkins>"

        }

    } catch (err) {
        slackSend color: "danger", message: "Build failed :face_with_head_bandage: \n`${env.JOB_NAME}#${env.BUILD_NUMBER}` <${env.BUILD_URL}|Open in Jenkins>"


    }


}
