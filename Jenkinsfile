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

        

    }

}
