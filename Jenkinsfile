pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        
        stage('Git Checkout') {
            steps {
                git 'https://github.com/kabirbaidhya/react-todo-app.git'
            }
        }
        
        stage('npm version') {
            steps {
                nodejs('NodeJS_16') {
                sh 'npm -version'
                }
            }
        }
        
        stage('Install Dependencies') {
            steps {
                nodejs('NodeJS_16') {
                sh 'npm install'
                }
            }
        }

        stage('Run Tests') {
            steps {
                nodejs('NodeJS_16') {
                sh 'npm test'
                }
            }
        }

        stage('Start the application') {
            steps {
                nodejs("NodeJS_16") {
                sh 'npm start &'
                }
            }
        }
    }
}

