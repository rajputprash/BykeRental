// Declarative //
pipeline {
    agent any { label "kubepod" }

    stages {
        stage('Checkout source') {
            steps {
                git url: 'https://github.com/rajputprash/BykeRental', branch: 'test-deploy-stage'
            }
        }
        stage('Deploy APP') {
            steps {
             script {
                kubernetesDeploy(configs:  "nginx.yaml", "jenkins-data")
            }
          }
        }
      
    
   

