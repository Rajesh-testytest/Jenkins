pipeline {
    agent any
    stages {
        stage ('success/failure') {
            when {
                expression {env.GIT_BRANCH == 'origin/master'}
            }
            steps {
                echo "Hello, Rajesh"
            }
        }
    }
}
