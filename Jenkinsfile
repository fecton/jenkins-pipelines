pipeline{
    agent any
    options{
        timestamps()
    }
    environment{
        name = "John"
        surname = "Smith"
        DEPLOY_TO = "production"
    }
    stages{
        stage("Build"){
            when {
                equals expected: "jeff", actual: DEPLOY_TO
            }
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