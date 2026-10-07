pipeline {
    agent any
    environment {
        JAVA_HOME = 'C:\\Program Files\\Java\\jdk-21.0.12.1'
        PATH = "${env.JAVA_HOME}\\bin;${env.PATH}"
    }
    
    tools {
        maven 'Maven3'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Renu-Kumar-M/maven-2.git'
            }
        }
        stage('Compile') {
            steps {
                bat 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
}
