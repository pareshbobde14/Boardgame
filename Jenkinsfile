pipeline {
    agent any
    
    tools{
        jdk "jdk17"
        maven "maven3"
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'patch', url: 'https://github.com/pareshbobde14/Boardgame.git'
            }
        }
        
         stage('Compile') {
            steps {
                sh "mvn clean compile"
            }
        }
        
         stage('Build') {
            steps {
                sh "mvn clean package"
            }
        }
