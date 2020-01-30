pipeline {
    agent any
    stages {      
        stage('Upload to AWS') {
            steps{
                withAWS(region:'us-west-2', credentials:'aws-static') {
                    s3Upload(file:'index.html', bucket:'jenkin-pipeline-udacity')
                    sh 'echo "uploaded files to s3"'
                }
            }
        }
    }
}
