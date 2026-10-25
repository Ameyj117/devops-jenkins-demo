
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the application...'
                bat 'if not exist index.html exit /b 1'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                bat 'if not exist deploy mkdir deploy'
                bat 'copy /Y index.html deploy\\index.html'
            }
        }
    }
}
