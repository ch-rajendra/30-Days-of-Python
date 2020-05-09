pipeline {
  agent any
  stages {
    stage("Build and Test") {
      steps {
        script {
          parallel linux: {
            node("linux_build") {
              echo "Inside for loop 1"
            }
            node("linux_test") {
              echo "Inside for loop 2"
            }
          },
          windows: {
            node("windows_build") {
              echo "Inside for loop 3"
            }
            node("windows_test") {
              echo "Inside for loop 4"
            }
          }
        }
      }
    }
  }
}
