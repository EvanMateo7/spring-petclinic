pipeline {
    agent any
    environment {
        COUNT = 0
    }
    stages {
        stage('1') {
            when { branch 'master' }
            steps{
                script {
                    echo env.COUNT
                    env.COUNT = "777"
                    echo env.COUNT
                    bat 'set'
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