pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Aboss7777/DevOps_pracs.git'
            }
        }


        stage('Deploy to XAMPP') {
            steps {
                // Copy the HTML files to XAMPP htdocs directory
                bat 'xcopy /E /Y .\\*.html "C:\\xampp\\htdocs\\"'
            }
        }
    }

    post {
        success {
            echo 'Deployment successful!'
        }
        failure {
            echo 'Deployment failed!'
        }
    }
}
