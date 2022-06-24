pipeline {
    agent any
    tools {
        maven "MAVEN"
    }
    
    stages {
        stage("Clone code from GitHub") {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'Git_CRED', url: 'https://github.com/dhakad0502/jenkins-nexus.git']]])
            }
        }
        stage("Maven Build") {
            steps {
                script {
                    sh "mvn package -DskipTests=true"
                }
            }
        }
        
            }
}
