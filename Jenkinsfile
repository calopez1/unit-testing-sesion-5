pipeline {
    agent any
    stages {
        stage ('Build Backend') {
            environment {
                mvnHOME = tool 'MAVEN_HOME'
            }
            steps {
				sh  "${mvnHOME}/bin/mvn clean package -DskipTests=true"	
            }
        }
		stage ('Run test') {
            environment {
                mvnHOME = tool 'MAVEN_HOME'
            }
            steps {
				    sh  "${mvnHOME}/bin/mvn test"	
            }
        }
		stage ('Sonar Analysts') {
            environment {
                scanerHOME = tool 'SONAR_SCANER'
            }
            steps {
				withSonarQubeEnv('SONAR_LOCAL'){
				    sh  "${scanerHOME}/bin/sonar-scanner -e -Dsonar.projectKey=backend -Dsonar.host.url=http://sonarqube:9000 -Dsonar.login=1296e651ae0f526d9bc8061faf317f3707678ec0 -Dsonar.java.binaries=target -Dsonar.coverage.exclusions=**/src/test/**,**/entity/**"	
				}
            }
        }
    }
}