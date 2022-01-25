pipeline {
    agent { docker { image 'php:7.0-apache' } }
    stages {
        stage('build') {
            steps {
                sh 'docker build -t hello-word-php-apache .'
                sh 'docker run -p 8081:80 hello-word-php-apache'
            }
        }
    }
}
