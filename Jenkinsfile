pipeline {
    agent any

    tools {
        maven 'MAVEN3'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'master',
                url: 'https://github.com/tengaleh/simple-java-maven-app.git'
            }
        }

        stage('Build with Maven') {
            steps {
                sh 'mvn clean package'
            }
        }
    }

    post {
        success {
            echo 'Build Successful!'
        }
        failure {
            echo 'Build Failed!'
        }
    }
}
