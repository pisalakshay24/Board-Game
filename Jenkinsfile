pipeline {
    agent any

    tools {
        maven 'maven 3.9'
        jdk 'JDK17'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git 'https://github.com/pisalakshay24/Board-Game.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
