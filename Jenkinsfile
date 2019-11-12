pipeline {
    agent any
    stages {
	stage('Upload to aws') {
	    steps {
		withAWS(credentials:'aws-static',region:'eu-central-1') {
		    s3Upload(file:'index.html',bucket:'rodrigorr-pipeline')
		}
	    }
	}
    }
}
