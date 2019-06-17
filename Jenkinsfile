
	pipeline{
		
		agent any
		
		stages{
			
			stage("Build"){
				steps{
					echo 'build stage'
					bat 'mvn clean package'
				}
				posts{
					success{
						echo 'now archiving'
						archiveArtifacts artifacts: '**/target/*.war'
					}
				}
				
			}
			stage("Deployments"){
				steps {
					echo 'deploying to staging'
					
				}
			}
		}
	}
