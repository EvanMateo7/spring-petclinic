pipeline {
    agent any
    stages {
        stage('1') {
            when { branch 'master' }
            steps{
                script {
                    bat """IF NOT EXIST count.txt (echo 0 > count.txt)
                            set /p OLD=<count.txt
                            echo %OLD%
                            set /a NEW=OLD+1
                            echo %NEW%"""
                    stdout = bat(returnStdout: true, script: 'set')
                    echo stdout
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