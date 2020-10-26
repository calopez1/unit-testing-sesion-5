tools {
    maven 'MAVEN_HOME'
}
pipeline{
	agent any
	stages {
		stage ('Build backend') {
			steps {
			 		sh 'mvn clean package -DskipTests=true'
			}
		}
	}
}

