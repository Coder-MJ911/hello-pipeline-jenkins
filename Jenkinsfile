// CODE_CHANGE = getGitChanges()
pipeline {
    agent any
    environment {
        NEW_VERSION = '1.0'
    }
    stages {
        stage('Build') {
//             when {
//                  expression {
//                     CODE_CHANGE == true
//                  }
//             }
            steps {
                echo 'application build...'
                echo "building version is ${NEW_VERSION}"
            }
        }
        stage('Test'){
            steps {
                echo 'application test...'
            }
        }
        stage('Deploy') {
//             when {
//                 expression {
//                     env.BRANCH_NAME == 'master'
//                 }
//             }
            steps {
                echo 'application deploy'
            }
        }
    }
    post {
        always {
            echo 'send the email to pusher to say pipeline is done...'
        }
        failure {
            echo 'pipeline build failed...'
        }
        success {
            echo 'pipeline build successful...'
        }
    }
}