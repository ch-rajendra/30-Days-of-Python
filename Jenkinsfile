pipeline {
  agent any
  stages {
    stage('Build Compliance') {
      steps {
        echo 'from build compliance'
      }
    }
  }

    stage('Import') {
      parallel {
        stage("Import") { }; stage("AutomatedTests") { }; stage("JFrogPublish") { } 
        stage("Import_SA_Python2.x") { }; stage("AutomatedTests") { }
        stage("Import_SA_Python3.x") { }; stage("AutomatedTests") { }
        
      }
    }

  }

