pipeline {
    agent any
    tools {
        jdk 'jdk-21'
    }
    stages {
        stage('Git Start') {
            steps {
                echo 'Git pipeline started'
                git branch: 'main', url: 'https://github.com/1ms24mc102/new-repo/'
            }
        }
        stage('Git End') {
            steps {
                echo 'Git pipeline completed...'
            }
        }
        stage('Compiling') {
            steps {
                echo 'Compiling source code...'
                sh 'javac Hello.java'
            }
        }
        stage('Running') {
            steps {
                echo 'Running unit test...'
                sh 'java Hello'
            }
        }
    }
}
