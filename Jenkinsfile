pipeline{
    agent none
    stages{
        stage("Build"){
            steps{
                agent any
                options {
                    skipDefaultCheckout()
                }
                timestamps{
                    echo "========executing Build ========"
                    echo "Hello"
                    echo "World"
                }
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
        stage("Test") {
            steps {
                echo "Test stage"
            }
        }
    }
}