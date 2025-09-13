pipeline{
    agent any
    environment{
        DIRECTORY_PATH = "./path/this/pipeline"
        TESTING_ENVIRONMENT = "Jenkins"
        PRODUCTION_ENVIRONMENT = "jenkins 6.1 pipeline"
    }
    stages{
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
        stage('Test'){
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
        stage('Code Quality Check'){
            steps{
                echo "==========Executing CQC=========="
                echo "Check the quality of the code"
            }
            post{
                always{
                    echo "Result"
                }
                success{
                    echo "++++++++++Executed CQC Successfully++++++++++"
                }
                failure{
                    echo "----------CQC Failed----------"
                }
            }
        }
        stage('Deploy'){
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
        stage('Approval'){
            steps{
                echo "==========Executing Approval=========="
                timeout(time:12, unit: 'SECONDS'){
                    sleep 10
                }
            }
            post{
                always{
                    echo "Result"
                }
                success{
                    echo "++++++++++Executed Approval Successfully++++++++++"
                }
                failure{
                    echo "----------Approval Failed----------"
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
    }
}