pipeline {
    agent any
    stages {
        stage ('success/failure') {
            steps{
                sh 'printenv'
                echo $GIT_BRANCH
            }
        }
    }
}
