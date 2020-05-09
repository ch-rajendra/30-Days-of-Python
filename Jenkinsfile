pipeline {
  agent any
  stages {
    stage("Build and Test") {
      steps {
        script {
          parallel 
          linux: {
            stage("linux_build") {
              echo "Inside for loop 1"
            }
            stage("linux_test") {
              echo "Inside for loop 2"
            }
          },
          windows: {
            stage("windows_build") {
              echo "Inside for loop 3"
            }
            stage("windows_test") {
              echo "Inside for loop 4"
            }
          }
        }
      }
    }
  }
}
