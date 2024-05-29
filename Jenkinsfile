pipeline{
    agent any 
    tools{
        maven "Maven_3_5_2"
    }
    stages{
        stage('CompileandRunSonarAnalysis') {
            steps {	
		    withCredentials([string(credentialsId: 'sonar_token1', variable: 'sonar_token1')]) {
    sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=tech223 -Dsonar.organization=tech223 -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=$sonar_token1'
}

		
			}
        } 
	  //   stage('RunSCAAnalysisUsingSnyk') {
   //          steps {		
			// 	withCredentials([string(credentialsId: 'SNYK_TOKEN', variable: 'SNYK_TOKEN')]) {
			// 		sh 'mvn snyk:test -fn'
			// 	}
			// }
   //  }	
   //      stage('Build'){
   //          steps{
   //              withDockerRegistry(
   //                  [credentialsId:"dockerlogin", url: ""]
   //              )  {
   //                  script{
   //                  app = docker.build("asg")
   //                  }
   //              }
   //          }
   //      }

   //      stage('Push'){
   //          steps{
   //              script{
   //                  docker.withRegistry("https://533267174558.dkr.ecr.us-west-2.amazonaws.com", "ecr:us-west-2:5008dffe-01e2-4643-8139-f5b375620f0a"){
   //                      app.push("latest")
   //                  }
                    
                    
   //              }
   //          }
        // }
    }

    
}
