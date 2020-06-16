pipeline {
  agent any
  	stages {
	stage ('Lint HTML'){
	steps {
		sh 'pwd'
		sh 'tidy -q -e *.html'
		}
			}
	stage ('Upload to AWS.'){
		steps {
            withAWS(credentials: 'aws-static' ,region: 'us-west-2' ) {
                 s3Upload(bucket:'jenkins-udacity-p3', includePathPattern:'**/*');
																	 }
				}
	       }
		}
}
