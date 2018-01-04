pipeline {
    agent any
    stages {
        stage('Preparation') { 
		steps{
			git 'https://github.com/AdamsEatin/JenkinsTask.git'
			def mvnHome = tool 'M3'
			}
		}
        stage('build') {
            steps {
				bat(/"${mvnHome}\bin\mvn.cmd" install -DskipTests/)
			}
		}
		stage('Testing') {
			steps{
				bat(/"${mvnHome}\bin\mvn.cmd" -Dmaven.test.failure.ignore clean package/)
			}
		}
    }
}
