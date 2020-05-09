pipeline {
  agent any
  stages {
    stage("Build") {
      steps {
          echo "From build step"
      }
      }
    stage("Parallel_Import")
    { 
    parallel [
          linux: {
            stage("linux_build") {
              echo "Inside linux_build"
            }
            stage("linux_test") {
              echo "Inside linux_test"
            }
          },
          windows: {
            stage("windows_build") {
              echo "Inside windows_build"
            }
            stage("windows_test") {
              echo "Inside windows_test"
            }
          }
    ]
    }
        }
      }


