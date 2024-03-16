pipeline {
	agent{
	label 'mens-slave'
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/harry/appfiles/apache-tomcat-9.0.86/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			sh 'cp target/myntra.war  /home/aishu/extracted/apache-tomcat-9.0.86/webapps'
			}}	
}}
