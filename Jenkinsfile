pipeline {
    agent any
    stages {
        stage ('Build Backend') {
            environment {
                mvnHOME = tool 'MAVEN_HOME'
            }
            steps {
		sh  "${mvnHOME}/bin/mvn test"	
            }
        }
    }
}