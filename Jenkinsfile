pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ newWrong.cpp -o output'
                echo 'Build Stage Successful'
            }
        }
        
        stage('Test') {
            steps {
                sh './output'
                echo 'Test Stage Successful'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
