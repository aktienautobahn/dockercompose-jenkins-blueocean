pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clean workspace before cloning
                cleanWs()
                
                // Clone or pull the repository
                git url: 'https://github.com/aktienautobahn/jenkins-dockercompose.git', branch: 'main'
            }
        }
        
        stage('Build') {
            steps {
                // Echo "Hello World!"
                echo 'Hello World!'
            }
        }
    }

    post {
        always {
            // Clean up workspace after build
            cleanWs()
        }
    }
}