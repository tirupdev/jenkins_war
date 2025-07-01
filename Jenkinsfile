pipeline {
    agent any
    stages {    # Define the stages of the pipeline
        stage('Checkout Code') { # Checkout the code from GitHub
            steps {
                git branch: 'main', url: 'https://github.com/tirupdev/gha_ec2tomcat-war.git'
            }
        }
        stage('Build WAR') {    # Build the WAR file using Maven
            steps {
                sh 'mvn clean package' # This command cleans the project and builds the WAR file
            }
        }
    }
}
