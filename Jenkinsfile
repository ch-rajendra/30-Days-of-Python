pipeline{
    agent any
stages {
    stage('Build') {
      steps {
        echo 'This stage will be executed first.'
      }
    }
    }
parallel (
  "DCA": {
    stage("DCA_Import") {
      stage("one-child1") {
        println "one-child1"
      }
      stage("DCA_AXIS_TESTS") {
        println "one-child2"
      }
    }
  },
  "SA_Python2.x": {
    stage("SA_Python2.x_Import") {
        println "two-child1"
      }
      stage("SA_Python2.x_Tests") {
        println "two-child2"
      }
  },
  "SA_Python3.x": {
    stage("SA_Python3.x_Import") {
       println "three-child1"
      }
      stage("SA_Python3.x_Tests") {
        println "three-child2"
      }
  }
) 
}
