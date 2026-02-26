pipeline {
    agent any // Or a specific agent with Node.js installed, or a Docker image (e.g., agent { docker { image 'node:20-alpine' } })
    stages {
        stage('Build') {
            steps {
                sh 'npm install' // Installs dependencies
                sh 'npm run build' // Creates a production-ready build in the 'build' folder
            }
        }
        stage('Test') {
            steps {
                // Assuming you have tests configured in your package.json
                sh 'npm test' // Runs your application tests
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps here (e.g., deploy to AWS S3, Heroku, or a server via SSH)
                echo 'Deployment stage (e.g., copy build artifacts to server)'
            }
        }
    }
}
