pipeline {
    agent any
    tools {
        maven "MAVEN"
    }
    
    stages {
        stage("Build Maven") {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'Git_CRED', url: 'https://github.com/dhakad0502/jenkins-nexus.git']]])
                sh "mvn package -DskipTests=true"
            }
        }
        
   }
}
