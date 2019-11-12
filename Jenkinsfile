pipeline {
    agent any
    stages {
	stage('lint html') {
	    steps { 
		tidy -q -e *.html 
	    }
	}
	stage('upload to aws') {
	    steps {
		withAWS(credentials:'aws-static',region:'eu-central-1') {
		    s3Upload(file:'index.html',bucket:'rodrigorr-pipeline')
		}
	    }
	}
    }
}
