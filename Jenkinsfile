pipeline {
    agent any
    stages {
        stage ('success/failure') {
            when {
                expression {env.GIT_BRANCH == 'origin/development'}
            }
            steps {

 //                  echo env.GIT_PREVIOUS_COMMIT
 //                  echo env.GIT_COMMIT
 //                  sh 'git status'
                   sh 'git log $GIT_PREVIOUS_COMMIT..$GIT_COMMIT --pretty=format:%cE'
            }
        }
     }

    post{
        failure{
            emailext(
                subject: "${env.JOB_NAME} [${env.BUILD_NUMBER}] Failed",
                body:"""<p> "${env.JOB_NAME} [${env.BUILD_NUMBER}] Failed" </p> """,
                to: "rajeshayaldasani.cse18@gmail.com"
                )
                }
        success{
            emailext(
                subject: "${env.JOB_NAME} [${env.BUILD_NUMBER}] Success",
                body:"""<p> "${env.JOB_NAME} [${env.BUILD_NUMBER}] Success" </p> """,
                to: "rajeshayaldasani.cse18@gmail.com"
                )
                }
    }
}

