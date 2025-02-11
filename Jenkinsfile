pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', 
                    credentialsId: 'git-token', 
                    url: 'https://git-token@github.com/yourusername/Jenkins-Timestamp.git'
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
