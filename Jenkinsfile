pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ ./main/hello.cpp -o PES1UG21CS828'
                build job: 'PES1UG21CS831-1'
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG21CS831'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deployment stage"'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
