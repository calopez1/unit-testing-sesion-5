tools {
    maven 'MAVEN_HOME'
}
pipeline{
	agent any
	stages {
		stage ('Build backend') {
			withMaven(maven: 'mvn') {
			 		sh 'mvn clean package -DskipTests=true'
			}
		}
	}
}

