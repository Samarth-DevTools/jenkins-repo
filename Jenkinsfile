pipeline {
    agent any

    tools {
        // This name must match exactly the name you gave in Global Tool Configuration
        nodejs 'node20' 
    }

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