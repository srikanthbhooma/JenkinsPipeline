pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Repository Checked Out'
            }
        }

        stage('Compile') {
            steps {
                bat 'gcc add.c -o add.exe'
            }
        }

        stage('Run') {
            steps {
                bat 'add.exe'
            }
        }

    }

    post {

        success {
            echo 'Pipeline Executed Successfully'
        }

        failure {
            echo 'Pipeline Failed'
        }

    }

}