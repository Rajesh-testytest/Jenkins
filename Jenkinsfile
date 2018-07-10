pipeline {
    agent any
    stages {
        stage ('success/failure') {
            steps{
                sh 'git branch'
                sh 'git checkout master'
                sh 'git log'
                $GIT_BRANCH
            }
            
        }
    }
}
