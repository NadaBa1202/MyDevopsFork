pipeline {
    agent any
    tools {
        jdk 'JDK21'
    }
    stages {
        stage('Checkout code') {
            steps {
                git branch: 'master', url: 'https://github.com/NadaBa1202/MyDevopsFork'
            }
        }
        stage('Compile code') {
            steps {
                sh 'javac src/application/test.java'
            }
        }
        stage('Execute code') {
            steps {
                dir('src') {
                    sh 'java application.test'
                }
            }
        }
        stage('display message') {
            steps {
                echo 'Hello Github'
            }
        }
    }
}
