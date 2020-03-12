pipeline {
    agent any
    stages {
        stage('1') {
            when { branch 'master' }
            steps{
                script {
                    bat '''IF NOT EXIST count.txt (echo 0 > count.txt)
                            set /p OLD=<count.txt
                            echo %OLD%'''
                    def count = bat(script: '@echo %OLD%', returnStdout: true)
                    echo count
                    echo bat(returnStdout: true, script: 'set')
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