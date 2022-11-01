pipeline{
    agent{
        //label "agent1"
        docker{
            image 'node:latest'
            args '-p 3000:3000'
        }
    }
    environment{
        CI=true
    }
    stages{
        stage("build"){
            steps{
                //echo "========executing A========"
                sh 'npm install'
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
            }
        }
        
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}