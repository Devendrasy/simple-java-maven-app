pipeline {

    agent any
	tools { 
        maven 'M2' 
        jdk 'Java8'	

    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    
     stage('Sonar Qube analysis') {
            steps {
                sh 'mvn sonar:sonar -Dsonar.host.url=http://localhost:9000/sonar -Dsonar.projectName=MyProject -Dsonar.projectVersion=1.0 -Dsonar.projectKey=myproject -Dsonar.sources=. -Dsonar.java.binaries=. -Dsonar.tests=. -Dsonar.test.inclusions=**/*Test*/** -Dsonar.exclusions=**/*Test*/**'
            } 
        }       
    }	
}
