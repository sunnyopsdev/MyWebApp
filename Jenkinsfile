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

		
			stage ('dev') {
			
				steps{			
					echo "it is dev build "			
				}
		
			}
				
	}
}