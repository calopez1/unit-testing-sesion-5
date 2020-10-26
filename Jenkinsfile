pipeline{
	agent any
	stages {
		stage ('Build backend') {
			steps {
				step {
			 		sh 'mvn clean package -DskipTests=true'
				}
			}
		}
	}
}