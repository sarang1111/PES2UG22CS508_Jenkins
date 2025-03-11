pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o pes2ug22cs508_4 main.cpp'
                echo 'Build Stage Successful'
            }
        }
        
        stage('Test') {
            steps {
                sh './pes2ug22cs508_4'
                echo 'Test Stage Successful'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'cp pe2ug22cs508_4 /tmp/'
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
