pipeline {
    agent any
    stages {
        stage ('success/failure') {
//            when {
//                expression {env.GIT_BRANCH == 'origin/development'}
//                branch 'origin/master'
//            }
            steps {
                sh git branch -a
            }
        }
    }
}
