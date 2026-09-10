pipeline {
    agent { label 'agent-1' }
    
    tools {
        maven 'maven3.9'
        jdk 'jdk'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/jaiswaladi246/Boardgame.git'
            }
        }
        stage('Compile'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn package'
            }
        }
    }
}
