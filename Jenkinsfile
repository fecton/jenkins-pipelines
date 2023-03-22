pipeline{
    agent any
    options { skipDefaultCheckout() }
    stages{
        stage("Build"){
            steps{
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