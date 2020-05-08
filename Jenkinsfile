pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'This stage will be executed first.'
      }
    }

    stage('Import') {
      parallel {
        stage('Import') {
          steps {
            sleep 2
          }
        }

        stage('DCA Import') {
          steps {
            echo 'from dca import'
          }
        }

        stage('SA_Python2.x_Import') {
          steps {
            echo 'python2.x'
          }
        }

        stage('SA_Python3.x_Import') {
          steps {
            echo 'from python3.x SA version'
          }
        }

      }
    }

  }
}