pipeline {
  agent any
  options {
	  withAWS(credentials:'aws-static')
  }
  stages {
    stage('Upload to AWS.') {
        steps {
          s3Upload(file:'index.html', bucket:'udacity-devops-course-aleopold', path:'/index.html')
        }
    }
  }
}
