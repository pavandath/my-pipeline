pipeline{
    agent any
    stages{
        stage ('Build'){
            steps{
                echo "Building the project"
            }
        }
        stage('CodeAnalysis'){
            steps{
                echo "Running Code Analysis"
            }
        }
        stage('DockerBuildNdPush'){
            steps{
                echo "Building and Pushing the image"
            }
        }
        stage('DeployToDev'){
            steps{
                echo "Deploying to Dev Environment"
            }
        }
        stage('DeployToTest'){
            steps{
                echo "Deploying to Test Environment"
            }
        }
        stage('DeployToStage'){
            steps{
                echo "Depoloying to Stage Environment"
            }
        }
        stage('DeployToProd'){
            options{
                timeout(time:300, unit:'SECONDS')
            }
            input {
                message "Do you want to Deploy?"
                ok "yes"
                submitter 'dath'                  //only pavan & dath users can be able to submit
            }
            
            steps{
                echo "Deploying to Production Environment"
            }
        }
    }
}
