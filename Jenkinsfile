pipeline{
    agent any
    options{
        timestamps()
    }
    environment{
        name = "jeff"
        surname = "Smith"
        DEPLOY_TO = "production"
    }
    stages{
        stage("Build"){
            when {
                not {
                    equals expected: "jeff", actual: name
                }
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