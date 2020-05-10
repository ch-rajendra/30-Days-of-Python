pipeline {
    agent none
    stages {
        stage('Build') {
            steps {
                echo 'This stage will be executed first.'
            }
        }
        stage('Import') {
            when {
                branch 'master'
            }
            failFast true
            parallel {
                stage('Branch A') {
                    
                    steps {
                        echo "On Branch A"
                    }
                }
                stage('Branch B') {
                    
                    steps {
                        echo "On Branch B"
                    }
                }
                stage('DCA_Import') {
                    
                    stages {
                        stage('Import_Content') {
                            steps {
                                echo "In stage Nested 1 within Branch C"
                            }
                        }
                        stage('DCA_Tests') {
                            steps {
                                echo "In stage Nested 1 within Branch C"
                            }
                        }
                        stage('Publish') {
                            steps {
                                echo "In stage Nested 2 within Branch C"
                            }
                        }
                    }
                }
            }
        }
    }
}
