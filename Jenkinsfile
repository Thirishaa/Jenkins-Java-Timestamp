pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', 
                    credentialsId: 'github-username-PAT', 
                    url: 'https://github-username-PAT@github.com/yourusername/Jenkins-Timestamp.git'
            }
        }
        stage('Compile Java Program') {
            steps {
                sh 'javac TimestampPrinter.java'
            }
        }
        stage('Run Java Program') {
            steps {
                sh 'java TimestampPrinter'
            }
        }
    }
}
