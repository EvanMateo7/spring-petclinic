pipeline {
    node {
        stages {
             stage('1') {
                if (env.BRANCH_NAME == 'master') {
                    echo '$env'
                } else {
                    echo 'stage 1 not aster'
                }
            }
             stage('2') {
                if (env.BRANCH_NAME == 'master') {
                    echo 'stage 2 master'
                } else {
                    echo 'stage 2 not aster'
                }
            }
        }
       
    }
}