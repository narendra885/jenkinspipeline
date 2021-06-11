pipeline {
    agent any
    stages {
        stage('Gitclone') {
            steps {
                // Get some code from a GitHub repository
                git credentialsId: 'gitlogins', url: 'https://github.com/narendra885/jenkinssample.git'
              }
         }
        stage('Build') {
            steps{
              //Build step with maven
              sh "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }    
        
    }
}
