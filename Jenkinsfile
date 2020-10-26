pipeline{
	agent any
	stages {
		stage ('Build backend') {
			sh 'mvn clean package -DskipTests=true'
		}
	}
}