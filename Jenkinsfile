pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/junaidahmedjagiridar24882-sketch/MyGradleApp.git'
            }
        }

        stage('Build') {
            steps {
                sh './gradlew build'
            }
        }

        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }

        stage('Run Application') {
            steps {
                sh './gradlew run'
            }
        }
    }

    post {
        success {
            echo 'Build successful!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
