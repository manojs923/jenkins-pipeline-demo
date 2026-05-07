pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo '===== STAGE 1: Getting the code ====='
                echo 'Jenkins is downloading your code from GitHub...'
            }
        }

        stage('Build') {
            steps {
                echo '===== STAGE 2: Building the application ====='
                sh 'mkdir -p output'
                sh 'echo "This is my app version 1.0" > output/app.txt'
                echo 'Build complete! Output file created.'
            }
        }

        stage('Test') {
            steps {
                echo '===== STAGE 3: Testing the application ====='
                sh 'cat output/app.txt'
                echo 'All tests passed!'
            }
        }

        stage('Deploy') {
            steps {
                echo '===== STAGE 4: Deploying the application ====='
                echo 'Sending app to server...'
                echo 'Deployment complete!'
            }
        }
    }

    post {
        success {
            echo '✅ Everything worked! Build was SUCCESSFUL!'
        }
        failure {
            echo '❌ Something went wrong! Build FAILED!'
        }
    }
}
