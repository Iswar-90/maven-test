pipeline {
 agent none
 stages{
  stage("build and SonarQube Analysis")
  {
   agent any
    steps {
	 withSonarQubeEnv('my-sonar-project')
	 {
	  sh "mvn clean package sonar:sonar -Dsonar.projectKey=STL-project -Dsonar.projectName='STL-project'"
	 }
	}
  }
 }
}
