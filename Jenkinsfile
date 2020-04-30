pipeline {
    agent any
    stage('Upload to AWS') {
            steps {
                retry(2){
                withAWS(region:'us-east-1',credentials:'aws-static'){
                    s3Upload(file:'index.html', bucket:'jenkinsproj', path:'')
                }
                }
            }
    }
}