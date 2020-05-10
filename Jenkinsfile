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
                stage('DCA') {                    
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
                 stage('SA3.x') {                    
                    stages {
                        stage('Import_SAPython3.x') {
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
                        stage('Import_SAPython2.x') {
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
