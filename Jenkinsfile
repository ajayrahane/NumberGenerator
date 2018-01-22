pipeline
{
agent 
{
	label "master"
	
}
		
		stages
		{
			stage('Intialize'){
			steps{
			bat '''
			echo "M2_HOME = %M2_HOME%"
			'''
					
			}
		}
		
		stage('Build'){
		steps
		{
		bat ' cd NumberGenerator & mvn package'
		}
		
		post {
		success {
		
		junit 'NumberGenerator/target/surefire-reports/*.xml'
		
		}
		
		}
		

}
}
}
