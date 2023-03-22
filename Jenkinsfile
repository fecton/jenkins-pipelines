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
                sh "printenv"
            }
        }
        stage("Test") {
            steps {
                echo "Test stage"
            }
        }
    }
}