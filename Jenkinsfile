pipeline{
    agent any
    options{
        timestamps()
    }
    environment{
        name = "John"
        surname = "Smith"
    }
    stages{
        stage("Build"){
            steps{
                echo "========executing Build ========"
                echo "Hello"
                echo "My name is ${name} ${surname}"
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