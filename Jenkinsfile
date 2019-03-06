// Jenkinsfile (Declarative Pipeline)
pipeline {
    agent { dockerfile true }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
                sh 'svn --version'
            }
        }
        stage('Docker') {
            steps {
                sh 'docker images'
                //sh 'svn --version'
            }
        }
    }
}
