pipeline{
        agent any
    stages {
        stage('Example') {
            steps { 
                echo 'mvn compile'
            }
        }
    }

    parallel (
  "first": {
    stage("JUnit") {
    }
    stage("Firefox") { 
    }
  },
  "second" : {
    stage("D3Unit") {
    }
    stage("Edge") {
    }
  },
  "third" : {
    stage("Safari") {
    }
  }
)
}
