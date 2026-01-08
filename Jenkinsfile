pipeline {
    agent any

    tools {
        maven 'MAVEN3'
    }

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/spring-projects/spring-petclinic.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
