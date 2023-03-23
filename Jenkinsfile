pipeline{
    agent any
    options{
        timestamps()
    }
    environment{
        version = "1.0"
        name = "jeff"
        surname = "Smith"
        DEPLOY_TO = "production"
    }
    stages{
        stage("Build"){
            when {
                allOf {
                    environment name: "version", value: "1.0"
                    environment name: "name", value: "jeff"
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