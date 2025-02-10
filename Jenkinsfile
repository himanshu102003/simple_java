pipeline {
    agent { label 'agent1' }

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
}
