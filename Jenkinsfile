pipeline {
    agent any
    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/adminj98/devops_project.git'
            }
        }
        stage('Run Pre-Commit') {
            steps {
                sh 'pip install pre-commit'
                sh 'pre-commit run --all-files'
            }
        }
        stage('Run Python App') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
}
