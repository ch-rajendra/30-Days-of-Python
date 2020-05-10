pipeline {
    agent none
    stages {
        stage('Build_Content') {
            steps {
                echo 'This stage will be executed first.'
            }
        }
        stage('Import_Content') {
            when {
                branch 'master'
            }
            failFast true
            parallel {
                stage('DCA') {                    
                    stages {
                        stage('DCA_Import') {
                            steps {
                                echo "In stage Nested 1 within Branch C"
                            }
                        }
                        stage('DCA_Tests') {
                            steps {
                                echo "In stage Nested 1 within Branch C"
                            }
                        }
                        stage('JFrog_Publish') {
                            steps {
                                echo "In stage Nested 2 within Branch C"
                            }
                        }
                    }
                }
                 stage('SA3.x') {                    
                    stages {
                        stage('Import_SA_Python3.x') {
                            steps {
                                echo "In stage Nested 1 within Branch C"
                            }
                        }
                        stage('SA_Tests') {
                            steps {
                                echo "In stage Nested 1 within Branch C"
                            }
                        }
                    }
                }
                 stage('SA2.x') {                    
                    stages {
                        stage('Import_SA_Python2.x') {
                            steps {
                                echo "In stage Nested 1 within Branch C"
                            }
                        }
                        stage('SA_Tests') {
                            steps {
                                echo "In stage Nested 1 within Branch C"
                            }
                        }
                       
                    }
                }
            }
        }
    }
}
