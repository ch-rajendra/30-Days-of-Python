pipeline {
  agent any
  stages {
    stage("Build") {
      steps {
          echo "From build step"
      }
    stage("Parallel_Import")   
    parallel 
          linux: {
            stage("linux_import") {
              echo "Inside linux_import"
            }
            stage("linux_test") {
              echo "Inside linux_test"
            }
          },
          windows: {
            stage("windows_import") {
              echo "Inside windows_import"
            }
            stage("windows_test") {
              echo "Inside windows_test"
            }
          }
        }
      }
 }

