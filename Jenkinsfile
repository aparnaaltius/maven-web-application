pipeline{

agent any

tools{
maven 'maven3.8.2'
}
stages{

  stage('CheckOutCode'){
    steps{
	git credentialsId: '5fb259b1-27d8-4d48-803c-f0b0fe4c0962', url: 'https://github.com/aparnaaltius/maven-web-application.git'
	}
  }
  

 stage('ExecuteSonarQubeReport'){
  steps{
  sh  "mvn clean sonar:sonar"
  }
  }
  
}//Stages Closing


}//Pipeline closing
