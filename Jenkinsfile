pipeline {
  agent any
  stages {
    stage('Upload to AWS.') {
      withAWS(credentials:'aws-static') {
        steps {
          s3Upload(file:'index.html', bucket:'udacity-devops-course-aleopold', path:'/index.html')
        }
      }
    }
  }
}
