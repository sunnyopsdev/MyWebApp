pipeline {
	agent any
	environment {
		env = dev
		
	}
	stages{
	
		stage ('clean')
		{
		
			steps
			{
				mvn clean
			}
		
		}
		parallel {
		
			stage ('dev') {
			
				steps{			
					mvn compile -Denv="dev"				
				}
		
			}
			
			stage ('qa') {
				steps{			
					mvn compile -Denv=qa				
				}
			
			}
		
		}

	
	}
}