pipeline{
    agent any
    stages{
        stage("Build"){
            options {
                timeout(time: 1, unit: 'SECONDS')
            }
            steps{
                echo "========executing Build ========"
                sleep 2
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========Build  executed successfully========"
                }
                failure{
                    echo "========Build  execution failed========"
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