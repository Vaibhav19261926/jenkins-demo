pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Cloning Repository'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                cp index.html /var/www/html/
                '''
            }
        }

        stage('Verify Deployment') {
            steps {
                echo 'Checking Apache Directory'
                sh 'ls -la /var/www/html/'
            }
        }
    }

    post {
        success {
            echo 'Website Successfully Deployed to Apache Server'
        }
    }
}