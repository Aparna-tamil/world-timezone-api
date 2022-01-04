pipeline
{
agent any
stages{
	stage('Build Application'){
	sreps{
	bat 'mvn clean install'
	}
	}
	
	stage('Deploy Application to Cloudhub'){
	steps{
	bat 'mvn package deploy -DmuleDeploy'
	}
	}
	
	stage('Perform Regression Testing'){
	steps{
	bat 'newman run C:\\Users\\abarnapp\\Postman\\WorldTimeZone.postman_collection.json --disable-unicode'
	}
	}

}
}