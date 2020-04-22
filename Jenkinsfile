pipeline{
    agent any
    stages{
        stage('Upload to AWS'){
            withAWS(credentials:'IDofAwsCredentials') {
                
                s3Upload(file:'index.html', bucket:'jenkins-test-nano', path:'/')
            }

        }
    }
}