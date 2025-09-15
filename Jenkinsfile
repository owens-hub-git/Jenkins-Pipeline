pipeline{
    agent any
    environment{
        DIRECTORY_PATH = "./path/this/pipeline"
        TESTING_ENVIRONMENT = "Jenkins"
        PRODUCTION_ENVIRONMENT = "jenkins 6.1 pipeline"
    }
    stages{ //jenkins
        stage('Build'){
            steps{
                echo "==========Executing Build=========="
                echo "Fetch the source code from the directory path: $DIRECTORY_PATH"
                echo "Compile the code and generate any neccessary artefacts"
            }
            post{
                always{
                    echo "Result"
                }
                success{
                    echo "++++++++++Executed Build Successfully++++++++++"
                }
                failure{
                    echo "----------Build Failed----------"
                }
            }
        }
        stage('Unit and Integration Tests'){
            steps{
                echo "==========Executing Test=========="
                echo "Unit test"
                echo "Integration tests"
            }
            post{
                always{
                    echo "Result"
                }
                success{
                    echo "++++++++++Executed Test Successfully++++++++++"
                }
                failure{
                    echo "----------Test Failed----------"
                }
            }
        }
        stage('Code Analysis'){
            steps{
                echo "==========Executing Code Analysis=========="
                echo "Check the quality of the code at $DIRECTORY_PATH"
            }
            post{
                always{
                    echo "Result"
                }
                success{
                    echo "++++++++++Executed Code Analysis Successfully++++++++++"
                }
                failure{
                    echo "----------Code Analysis Failed----------"
                }
            }
        }
        stage('Security Scan'){
            steps{
                echo "==========Executing Security Scan=========="
                echo "Scan the code for security concerns"
            }
            post{
                always{
                    echo "Result"
                }
                success{
                    echo "++++++++++Executed Security Scan Successfully++++++++++"
                }
                failure{
                    echo "----------Security Scan Failed----------"
                }
            }
        }
        stage('Deploy to Staging'){
            steps{
                echo "==========Executing Deploy=========="
                echo "Deploy the application to a testing environment specified by the environment variable: $TESTING_ENVIRONMENT"
            }
            post{
                always{
                    echo "Result"
                }
                success{
                    echo "++++++++++Executed Deploy Successfully++++++++++"
                }
                failure{
                    echo "----------Deployment Failed----------"
                }
            }
        }
        stage('Integration Test on Staging'){
            steps{
                echo "==========Executing Integration Test on Staging=========="
                timeout(time:12, unit: 'SECONDS'){
                    sleep 10
                }
            }
            post{
                always{
                    echo "Result"
                }
                success{
                    echo "++++++++++Executed Integration Test on Staging Successfully++++++++++"
                }
                failure{
                    echo "----------Integration Test on Staging Failed----------"
                }
            }
        }
        stage('Deploy to Production'){
            steps{
                echo "==========Executing Deploy to Production=========="
                echo "Deploy the code to the production environment variable: $PRODUCTION_ENVIRONMENT"
            }
            post{
                always{
                    echo "Result"
                }
                success{
                    echo "++++++++++Executed Deploy to Production Successfully++++++++++"
                }
                failure{
                    echo "----------Deploy to Production Failed----------"
                }
            }
        }
        stage('Random try'){
            steps{
                echo "==========test=========="
                timeout(time:12, unit: 'SECONDS'){
                    sleep 10
                }
            }
            post{
                always{
                    echo "Result"
                }
                success{
                    echo "++++++++++++++++++++"
                }
                failure{
                    echo "--------------------"
                }
            }
        }
    }

}




