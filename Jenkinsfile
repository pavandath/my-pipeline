//when condition (it executes whenever a condition is matched)
pipeline{
    agent any
    environment{
        DEPLOY_TO = 'production'
    }
    stages{
        stage('ProdDeploy'){
            when {
                environment name: 'DEPLOY_TO', value: 'production'   //when name is DEPLOY_TO and it's value matched to production steps will execute
            }
        steps{
            echo "Deploying to production"
        }
        }
    }
}
