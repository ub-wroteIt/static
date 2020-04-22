pipeline{
    agent any
    stages{
        stage('Upload to AWS'){
            steps{
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''    
            }
            withAWS(credentials:'IDofAwsCredentials') {
                def identity=awsIdentity();//Log AWS credentials
                s3Upload(file:'index.html', bucket:'jenkins-test-nano', path:'/')
            }

        }
    }
}