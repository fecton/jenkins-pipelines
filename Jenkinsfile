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
        stage("Build tag") {
            when{
                tag "2.0"
            }
            steps {
                echo "[+] Tag 2.0 was built successfully!"
            }
        }
        stage("Build master"){
            when {
                branch "main"
            }
            steps{
                echo "========executing Build ========"
                // sh "printenv"
            }
        }
        stage("Build dev"){
            when {
                branch "dev"
            }
            steps{
                echo "========executing Dev Build ========"
                // sh "printenv"
            }
        }
    }
}