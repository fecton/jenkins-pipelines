pipeline{
    agent any
    stages{
        stage("Build"){
            options {
                timestamps()
            }
            steps{
                echo "========executing Build ========"
                echo "Hello"
                echo "World"
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