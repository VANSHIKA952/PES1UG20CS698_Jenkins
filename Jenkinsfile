pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o obj PES1UG20CS698.cpp'
                build job : 'PES1UG20CS698-1'
                echo 'Build stage successful'
            }
        }
        stage('Test') {
            steps {
                sh './van'
                echo 'Test stage successful'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying "'
                echo 'Deployment successful'
            }
        }
    }
    post {
        failure {
          echo 'Pipeline failed'
                }
            
        
    }
}
