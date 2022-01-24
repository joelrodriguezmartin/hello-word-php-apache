pipeline {
    agent { docker { image 'php:7.4-cli' } }
    stages {
        stage('build') {
            steps {
                sh 'docker build -t hello-word-php-apache .'
                sh 'docker run -p 80:8081 hello-word-php-apache'
            }
        }
    }
}
