pipeline{
    agent any
    environment{
        DEPLOY_TO = 'production'
    }
    stages{
        stage ('DeploytoDev'){
            steps{
                echo "Deploying to dev environment"
            }
            }

        stage ('ProdDeploy'){
            when{
                allOf{
                    branch 'production'
                    expression name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps{
                echo "Deploying to production"
            }
            }
        }
    
}
