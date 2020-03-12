pipeline {
    agent any
    stages {
        stage('1') {
            when { branch 'master' }
            steps{
                script {
                    echo env.COUNT
                    bat 'set COUNT=123'
                    echo env.COUNT
                    if (env.BRANCH_NAME == 'master') {
                        bat 'mkdir testestest'
                    } else {
                        echo 'Not master'
                    }
                }
            } 
        }
        stage('2') {
            when { branch 'master' }
            steps{
                script {
                    if (env.BRANCH_NAME == 'master') {
                        echo 'master'
                    } else {
                        echo 'Not master'
                    }
                }
            } 
        }
    }
}