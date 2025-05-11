pipeline {
    agent any
    environment {
        // Customize these variables:
        GIT_REPO = 'https://github.com/Khizar20/PDFChabot.git'
        GIT_BRANCH = 'main'
        DOCKER_PROJECT_NAME = "pdfchat-${BUILD_NUMBER}"
    }
    stages {
        stage('Checkout Code') {
            steps {
                git branch: "${GIT_BRANCH}", 
                url: "${GIT_REPO}"
            }
        }
        stage('Build & Deploy') {
            steps {
                sh """
                docker-compose -p ${DOCKER_PROJECT_NAME} down || true  // Cleanup old containers
                docker-compose -p ${DOCKER_PROJECT_NAME} up -d --build
                """
            }
        }
    }
    post {
        always {
            cleanWs()  // Clean workspace after build
        }
    }
}
