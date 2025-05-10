pipeline{
    agent any
    stages{
        stage("Logging into AWS Console"){
            steps{
                withCredentials([string($class: 'AmazonWebServicesCredentialsBinding',credentialsId: 'AWS-CLI', variable: 'AWS_CREDS')]){
                    sh "echo 'hello world'"
                }
            }
        }
    }
}