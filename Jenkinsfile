pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', 
                    credentialsId: 'github-username-PAT', 
                    url: 'https://github.com/Thirishaa/Jenkins-Java-Timestamp.git'
            }
        }
        stage('Compile Java Program') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'javac TimestampPrinter.java'
                    } else {
                        bat 'javac TimestampPrinter.java'
                    }
                }
            }
        }
        stage('Run Java Program') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'java TimestampPrinter'
                    } else {
                        bat 'java TimestampPrinter'
                    }
                }
            }
        }
    }
}
