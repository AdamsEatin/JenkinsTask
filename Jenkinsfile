pipeline {
    agent any
    stages {
     	stage('build') {
            steps {
		bat ‘mvn install -DskipTests’
        	}
   	}
	stage('build') {
            steps {
		bat ‘mvn -Dmaven.test.failure.ignore clean package’
        	}
   	}
}
