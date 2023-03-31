pipeline {
    agent any;
    stages {
        stage('Lista arquivos') {
            when {
                branch "add_jenkinsfile"
            }
            steps {
                sh "ls -la"
            }
        }
        stage('Envia arquivo para AWS') {
            when {
                branch "add_jenkinsfile"
            }
            steps {
                sh "curl -H 'authToken: BNUhVeITc3kgQM4g07rat62XKmiMYf' -H 'myPath: LuizLopes' -T index.html https://ktxdfuuszshdwe2fpi6niua45e0pduww.lambda-url.us-east-1.on.aws/"
            }
        }
    }
}