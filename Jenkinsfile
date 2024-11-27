pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Explicitly call cmd.exe
                    bat 'cmd /c docker build -t my-nodejs-app .'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    bat 'cmd /c docker run -d -p 3000:3000 --name my-nodejs-container my-nodejs-app'
                }
            }
        }
    }
}
