#! groovy
pipeline{
    agent any

    stages {
        stage('Build'){
            steps {
                sh 'history'
            }
        }
        stage('Test') {
            steps {
                 sh 'echo hola'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mkdir deploy'
                sh 'cd deploy'
                sh 'touch nota.txt'
                sh 'echo hello nota >> nota.txt'
            }
        }
    }
}
