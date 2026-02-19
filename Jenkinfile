pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                echo 'Installing npm packages...'
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                echo 'Running unit tests...'
                sh 'npm test'
            }
        }

        stage('Build/Package') {
            steps {
                echo 'Packaging application...'
                // This simulates a build step, like creating a zip or docker image
                sh 'tar -czf app.tar.gz app.js package.json'
            }
        }
    }
}