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

		
			stage ('dev') {
			
				steps{			
					sh "/usr/bin/mvn compile install"		
				}
		
			}
				
	}
}