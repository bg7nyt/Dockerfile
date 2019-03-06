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
                //sh 'docker images'
                //sh 'svn --version'
                docker.withRegistry('http://192.168.0.157:5000') {
                    
                    def customImage = docker.build("php")
                    customImage.push()
                }
            }
        }
    }
}
