pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git credentialsId: 'github', url: 'https://github.com/VuPlayBoizz/Mediplus_Lite.git'
            }
        }
        stage('Check Docker') {
            steps {
                sh 'docker --version'
            }
        }
        stage('Push Docker Hub') {
            steps {
                withDockerRegistry(credentialsId: 'dockerhub', url: '') {
                    sh 'docker build -t nguyenbavu1902/web:1.0 .'
                    sh 'docker push nguyenbavu1902/web:1.0'
                }
            }
        }
    }
    // post {
    //     always {
    //         mail bcc: '', body: 'Deploy', cc: '', from: '', replyTo: '', subject: 'Test Jenkins', to: 'nguyenbavu1902@gmail.com'
    //     }
    // }
}
