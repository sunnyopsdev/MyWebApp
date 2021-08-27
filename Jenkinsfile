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
					echo "it is dev build "			
				}
		
			}
				
	}
}