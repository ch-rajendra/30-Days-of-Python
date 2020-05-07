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
        }

        stage('Import on SA 2018.08') {
          steps {
            echo 'import on SA with python2.x'
          }
        }

        stage('Import on SA 2020.09') {
          steps {
            echo 'import on SA'
          }
        }

      }
    }

  }
}