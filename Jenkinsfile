pipeline {

    agent any
	tools { 
        maven 'MAVEN' 
        jdk 'JAVA' 
	SonarQube Scanner 'Sonar_Scanner'	

    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn -B -DskipTests clean package'
            }
        }
    }
    stages {
        stage('Sonar Qube analysis') {
            steps {
                bat 'mvn sonar:sonar'
            } 
        }       
    }	
}
