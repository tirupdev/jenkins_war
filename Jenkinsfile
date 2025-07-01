pipeline {
    agent any
    stages {
        // Stage 1: Checkout Code from GitHub
        stage('Checkout Code') {
            steps {
                echo 'Checking out code from GitHub...'
                git branch: 'main', url: 'https://github.com/tirupdev/gha_ec2tomcat-war.git'
            }
        }

        // Stage 2: Build the WAR file using Maven
        stage('Build WAR') {
            steps {
                echo 'Building the WAR file using Maven...'
                sh 'mvn clean package'
            }
        }
    }
    post {
        // Notifications or cleanup steps after the pipeline
        always {
            echo 'Pipeline execution completed.'
        }
    }
}
