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
                anyOf{
                    branch 'production'
                    environment name: 'DEPLOY_TO', value: 'productionenv'
                }
            }
            steps{
                echo "Deploying to production"
            }
            }
        }
    
}
