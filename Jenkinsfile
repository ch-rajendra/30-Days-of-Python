pipeline {
  agent any
  stages {
    stage('Build Compliance') {
      steps {
        echo 'from build compliance'
      }
    }

    stage('Import') {
      parallel {
        stage('Import') {
          steps {
            echo 'From Import stage'
          }
        }

        stage('DCA Import') {
          steps {
            echo 'from dca import'
          }
          stages {
                        stage('DCA-Automated-tests') { steps {echo 'Executing Automated tests on Python2.x SA version'}}
                        stage('JFrog Publish') { steps {echo 'Executing Automated tests on Python2.x SA version'}}
                    }
        }

        stage('Import on SA 2018.08') {
          steps {
            echo 'import on SA with python2.x'
          }
          stages {
                        stage('Python2.x_Automated_Tests') { steps {echo 'Executing Automated tests on Python2.x SA version'}}
                    }
        }

        stage('Import on SA 2020.09') {
          steps {
            echo 'import on SA'
          }
          stages {
                        stage('Python3.x_Automated_Tests') { steps {echo 'Executing Automated tests on Python3.x SA version'}}
                    }
        }

      }
    }

  }
}
