pipeline {
    agent any
    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage("Clone code from GitHub") {
            steps {
               git branch: 'main', credentialsId: 'Git_CRED', url: 'https://github.com/dhakad0502/jenkins-nexus.git'
                sh "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
        
   }
}
