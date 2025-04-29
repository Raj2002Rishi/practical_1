pipeline {
    agent any

    environment {
        MY_ENV_VAR = 'This is a custom environment variable'
    }

    stages {
        stage('Clone Code from GitHub') {
            steps {
                git 'https://github.com/your-username/your-repo.git'
            }
        }

        stage('Run Shell Script') {
            steps {
                sh './your-script.sh'
            }
        }

        stage('Print Working Directory Content') {
            steps {
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Print Environment Variables') {
            steps {
                sh 'echo "MY_ENV_VAR is: $MY_ENV_VAR"'
                sh 'printenv'
            }
        }
    }

    post {
        always {
            echo "Pipeline execution finished."
        }
    }
}
