pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World multibranch pipeline'
            }
        }
        stage('cat Readme'){
            when {
                branch 'fix-*'
            }
            steps{
                sh '''
                 cat README.md
                 '''
            }
        }
    }
}