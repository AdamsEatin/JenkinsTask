pipeline {
    agent any
    stages {
        def mvnHome
        stage('Preparation') { // for display purposes
            git 'https://github.com/AdamsEatin/JenkinsTask.git'
         
            mvnHome = tool 'M3'
        }
        stage('build') {
            steps {
		bat(/"${mvnHome}\bin\mvn.cmd"Dmaven.test.failure.ignore clean package/)
            }
        }
    }
}
