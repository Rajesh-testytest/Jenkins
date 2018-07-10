pipeline {
    agent any
        stages {
           stage ('success/failure') {
               when {
                    expression { env.GIT_BRANCH == 'origin/development' }
                    }
            steps {
                echo 'hello'
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
    }
}

