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

        "DCA_Import" : { stage("Import") { }; stage("AutomatedTests") { }; stage("JFrogPublish") { } },
        "SA_Python2.x" : { stage("Import_SA_Python2.x") { }; stage("AutomatedTests") { }},
        "SA_Python3.x" : { stage("Import_SA_Python3.x") { }; stage("AutomatedTests") { }}
        
      }
    }

  }

