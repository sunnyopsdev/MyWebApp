pipeline {
	agent any
	environment {
		env="dev"
		
	}
	stages{
	
		stage ('clean')
		{		
			steps
			{
				sh "/usr/bin/mvn clean verify"
			}
		}

		
			stage ('compile') {
			
				steps{			
					sh "/usr/bin/mvn compile install"		
				}
		
			}
			
			stage ('deploy') {
			
				steps{	
					sh "./tomcat/apache-tomcat-9.0.50/bin/shutdown.sh"
					sh "rm -r /tomcat/apache-tomcat-9.0.50/webapps/MyWebApp*"		
					sh "cp /var/lib/jenkins/workspace/my-web-app_app-dev/target/MyWebApp.war /tomcat/apache-tomcat-9.0.50/webapps/ "
					sh "./tomcat/apache-tomcat-9.0.50/bin/startup.sh"			
				}
		
			}
				
	}
}