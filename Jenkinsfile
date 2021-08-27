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
				/usr/bin/mvn clean
			}
		
		}

		
			stage ('dev') {
			
				steps{			
					echo "it is dev build "			
				}
		
			}
				
	}
}