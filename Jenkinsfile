pipeline {
    agent any
    options {
        timeout(time: 5, unit: 'MINUTES')       // Pipeline will timeout after 5 minutes
        retry(2)                                // Retry the pipeline twice if it fails                          // Add timestamps to console output
        disableConcurrentBuilds()               // Prevent concurrent builds
    }
    stages {
        stage('Build'){
          steps {
            script {
                bat 'echo starting Hello world pipeline'
                bat 'javac Hello.java'
            }
        }
    }
    stage('Execute Script'){
      steps{
        script{
          bat 'java Hello'
        }
      }
    }
  }
    environment {
        WRAP_TIME = 'timestamps'
    }
}
