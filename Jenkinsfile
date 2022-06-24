pipeline {
    agent any
    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "MAVEN"
    }

    stages {
        stage("Clone code from GitHub") {
            steps {
               checkout([$class: 'GitSCM', 
                         
                    branches: [[name: '*/main']], extensions: [], 
                         
                    userRemoteConfigs: [[credentialsId: 'Git_CRED', url: 'https://github.com/dhakad0502/jenkins-nexus.git']]])
            }
        }
       stage("Maven Build") {
            steps {
                script {
                    sh "mvn -Dmaven.test.failure.ignore=true clean package"
                }
            }
        } 
   }
}
