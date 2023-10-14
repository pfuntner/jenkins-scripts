pipeline {
    agent any

    stages {
        stage('Hello') {
            withCredentials([string(credentialsId: 'SECRET_TEXT', variable: 'SECRET_TEXT')]) {
                steps {
                    echo 'Hello World'
                    sh 'hostname'
                    sh 'echo "$SECRET_TEXT" | gzip | base64"'
                }
            }
        }
    }
}
