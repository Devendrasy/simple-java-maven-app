pipeline {

    agent any
	tools { 
        maven 'MAVEN' 
        jdk 'JAVA'	

    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn -B -DskipTests clean package'
            }
        }
    
     stage('Sonar Qube analysis') {
            steps {
                bat 'mvn sonar:sonar -Dsonar.host.url=http://localhost:9000/sonar -Dsonar.projectName=MyProject -Dsonar.projectVersion=1.0 -Dsonar.projectKey=myproject -Dsonar.sources=. -Dsonar.java.binaries=. -Dsonar.tests=. -Dsonar.test.inclusions=**/*Test*/** -Dsonar.exclusions=**/*Test*/**'
            } 
        }       
    }	
}
