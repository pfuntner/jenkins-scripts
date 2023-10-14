pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                sh 'hostname'
                withCredentials([string(credentialsId: 'SECRET_TEXT', variable: 'SECRET_TEXT')]) {
                    sh 'echo "$SECRET_TEXT" | gzip | base64"'
                }
            }
        }
    }
}
