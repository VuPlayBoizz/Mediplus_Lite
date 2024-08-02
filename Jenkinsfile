pipeline {
    agent any
    stages{
        stage('Clone') {
            steps {
                git credentialsId: 'github', url: 'https://github.com/VuPlayBoizz/Mediplus_Lite.git'
            }
        }
        stage('Push Docker Hub') {
            steps {
                // This step should not normally be used in your script. Consult the inline help for details.
                withDockerRegistry(credentialsId: 'dockerhub', url: '') {
                    // some block
                    sh label: '', script: 'docker build -t nguyenbavu1902/web:1.0 .'
                    sh label: '', script: 'docker push nguyenbavu1902/web:1.0'
                }
            }
        }
    }
    // post {
    //     always {
    //         mail bcc: '', body: 'Deploy', cc: '', from: '', replyTo: '', subject: 'Tesst Jenkins', to: 'nguyenbavu1902@gmail.com'
    //     }
    // }
}
// Update v3
