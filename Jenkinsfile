pipeline {
    agent any
    tools {
	maven 'MAVEN'
    }
    stages {
        stage("Clone code from GitHub") {
            steps {
                script {
                       git branch: 'main', credentialsId: 'Git_CRED', url: 'https://github.com/dhakad0502/jenkins-nexus.git'
		}
            }
        }  
	  stage('Maven Build') {
	    steps {
		    sh "mvn -Dmaven.test.failure.ignore=true clean install"
	    }
	}
   }
}
    

