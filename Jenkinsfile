pipeline {
    agent any
    stages {
        stage('1') {
            when { branch 'master' }
            if (env.BRANCH_NAME == 'master') {
                echo 'master'
            } else {
                echo 'Not master'
            }
        }
        stage('2') {
            when { branch 'master' }
            if (env.BRANCH_NAME == 'master') {
                echo 'master'
            } else {
                echo 'Not master'
            }
        }
    }
}