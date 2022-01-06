pipeline
{
agent any
stages{
	stage('Build Application'){
	steps{
	bat 'mvn clean install'
	}
	}
	
	stage('Munit Testing Application'){
	steps{
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
	bat 'C:\\Users\\abarnapp\\AppData\\Roaming\\npm\\newman run C:\\Users\\abarnapp\\Postman\\WorldTimeZone.postman_collection.json --disable-unicode'
	}
	}

}
}