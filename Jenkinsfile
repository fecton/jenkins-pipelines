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
                expression {
                    name == "jeff"
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