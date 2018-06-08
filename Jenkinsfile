pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'xcodebuild -allowProvisioningUpdates'
          }
        }
        stage('Fastlane Test') {
          steps {
            sh 'fastlane tests'
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