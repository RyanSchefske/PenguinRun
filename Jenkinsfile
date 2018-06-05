pipeline {
  agent any
  stages {
    stage('Build') {
      environment {
        CI = 'true'
      }
      parallel {
        stage('Build') {
          steps {
            sh 'xcodebuild -allowProvisioningUpdates'
          }
        }
        stage('Print Build') {
          steps {
            echo 'Building...'
          }
        }
      }
    }
    stage('Finished Message') {
      steps {
        echo 'Done'
      }
    }
  }
}