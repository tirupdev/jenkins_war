pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/tirupdev/gha_ec2tomcat-war.git'
            }
        }
        stage('Build WAR') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
