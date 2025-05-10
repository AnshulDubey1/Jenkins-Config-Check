pipeline {
    agent any

    stages {
        stage("Logging into AWS Console") {
            steps {
                withCredentials([[
                    $class: 'AmazonWebServicesCredentialsBinding',
                    credentialsId: 'AWS-CLI'
                ]]) {
                    sh '''
                        echo "Access Key: $AWS_ACCESS_KEY_ID"
                        echo "Secret Key: $AWS_SECRET_ACCESS_KEY"
                        aws sts get-caller-identity
                    '''
                }
            }
        }
    }
}
