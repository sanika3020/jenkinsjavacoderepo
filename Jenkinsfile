pipeline {
    agent any
    
    tools {
        maven 'maven'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch:'main', url:'https://github.com/sanika3020/jenkinsjavacoderepo.git'  // Replace with actual repo
            }
        }

        stage('Build') {
            steps {
                dir('Javarepo1') {  // Change to actual repo folder
                    bat 'mvn clean package'
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed!'
        }
    }
}


