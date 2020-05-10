pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'from build'
      }
    }
  }
 stage('Import') {
    parallel {
        stage("Import_A") { 
            stages {
                stage("Tests_A") { steps { echo 'from A' } } 
                stage("Publish") { steps { echo 'from Publish' } }
            }
        }
        stage("Import_B") {
            steps { echo 'from B' } 
        }
    }
}   
}
