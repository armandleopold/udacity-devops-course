pipeline {
  agent any
  stages {
    stage('Lint HTML') {
      steps {
          sh 'tidy -q -e *.html'
      }
    }
    stage('Upload to AWS') {
      steps {
      	sh 'Hello world with aws creds.'
        withAWS(region: 'us-east-2', credentials: 'aws-static') {
          def identity = awsIdentity()
          s3Upload(file: './index.html', bucket: 'udacity-devops-course-aleopold')
        }
      }
    }
  }
}

