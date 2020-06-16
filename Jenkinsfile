pipeline {
  agent any
  	stages {
           dir('path/to/your/project/workspace'){

            pwd(); //Log current directory

            withAWS(region:'us-west-2') {

                 def identity=awsIdentity();//Log AWS credentials

                // Upload files from working directory 'dist' in your project workspace
                s3Upload(bucket:"jenkins-udacity-p3", workingDir:'dist', includePathPattern:'**/*');
            }

        };
    }
}
