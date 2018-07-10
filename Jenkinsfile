pipeline {
    agent any
    stages {
        stage ('success/failure') {
            steps{
                sh 'git status'
                sh 'git branch'
            }
        }
    }
}
