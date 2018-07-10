pipeline {
    agent any
    stages {
        stage ('success/failure') {
            steps{
                echo $GIT_BRANCH
            }
            when {
                branch 'master'
            }
            steps {
                echo "Hello, Rajesh!"
            }
        }
    }
}
