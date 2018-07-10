pipeline {
    agent any
    stages {
        stage ('success/failure') {
            when {
                expression {env.GIT_BRANCH == 'development'}
            }
            steps {
                echo 'hello'
            }
        }
    }
}
