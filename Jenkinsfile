pipeline {
    agent any

    stages {
        stage('Clone Code from GitHub') {
            steps {
                echo 'Code already checked out by Jenkins'
            }
        }

        stage('Run Shell Script') {
            steps {
                bat '''
                    echo Running a Windows batch script...
                    echo Hello from Jenkins on Windows!
                '''
            }
        }

        stage('Print Working Directory Content') {
            steps {
                bat 'dir'
            }
        }

        stage('Print Environment Variables') {
            steps {
                bat 'set'
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution finished.'
        }
    }
}
