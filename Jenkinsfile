pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'docker build -t hello-word-php-apache .'
                sh 'docker run -d --rm -p 8081:80 hello-word-php-apache'
            }
        }
        stage('Test'){
            steps{
                sh 'wget http://localhost:8081/'
            }
        }
    }
}
