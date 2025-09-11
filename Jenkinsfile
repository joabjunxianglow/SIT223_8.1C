pipeline{
    agent any
    environment{
        DIRECTORY_PATH = "/d/Deakin/Deakin_Work_2025_T2"
        TESTING_ENVIRONMENT = "AWS EC2"
        PRODUCTION_ENVIRONMENT = "AWS EC2"
    }
    stages{
        stage('Build'){
            steps{
                echo "Fetch the source code from $DIRECTORY_PATH"
                echo "Compile the code and generate any necessary artefacts using Maven"
            }            
        }
        stage('Tests'){
            steps{
                echo "Unit tests with JUnit"
                echo "Integration tests with Katalon"
            }
        }
        stage('Security Scan'){
            steps{
                echo "Conduct security check of application with FindSecBugs"
            }
        }
        stage('Deploy to Staging'){
            steps{
                echo "Deploy the application to $TESTING_ENVIRONMENT"
            }
        }
        stage('Tests on Staging'){
            steps{
                echo "Integration tests on staging with Katalon"
            }
        }
        stage('Deploy to Production'){
            steps{
                echo "Deployment of the code to $PRODUCTION_ENVIRONMENT is done"
            }
        }
    }
}