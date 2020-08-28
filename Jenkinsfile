pipeline {
    agent {
        label 'ip-172-31-36-119'
    }
    
    tools {
        maven 'M3'
    }
    
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('git pull') {
            steps {
            git credentialsId: 'jenkins', url: 'https://github.com/almadencloud/webapp'
            checkout scm
            sh 'echo ok'
            sh 'mvn clean'
            sh 'mvn package'
            }
        }
    }
}
