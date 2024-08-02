pipeline {
    agent any
    stages{
        stage('Clone') {
            steps {
                git credentialsId: 'github', url: 'https://github.com/VuPlayBoizz/Mediplus_Lite.git'
            }
        }
    //     stage('Push Docker Hub') {
    //         steps {
    //                 // This step should not normally be used in your script. Consult the inline help for details.
    //             withDockerRegistry(credentialsId: 'DockerHub', url: '') {
    //                 // some block
    //                 sh label: '', script: 'docker build -t nguyenbavu1902/web:latest .'
    //                 sh label: '', script: 'docker push -t nguyenbavu1902/web:latest'
    //             }
    //         }
    //     }
    }
    // post {
    //     always {
    //         mail bcc: '', body: 'Deploy', cc: '', from: '', replyTo: '', subject: 'Tesst Jenkins', to: 'nguyenbavu1902@gmail.com'
    //     }
    // }
}
// Update v2
//update