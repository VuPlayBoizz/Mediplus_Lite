pipeline {
    agent any
    stages{
        stage('Clone') {
            steps {
                git credentialsId: 'Github', url: 'https://github.com/VuPlayBoizz/Mediplus_Lite.git'
            }
        }
    }
}