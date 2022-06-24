pipeline {
    agent any
   
    stages {
        stage("Clone code from GitHub") {
            steps {
               git branch: 'main', credentialsId: 'Git_CRED', url: 'https://github.com/dhakad0502/jenkins-nexus.git'
            }
        }
        
   }
}
