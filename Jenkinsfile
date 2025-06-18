pipeline{
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
    stages{
        stage('ProdDeploy'){
            when {
                not{
                    equals expected: "prod", actual: "DEPLOY_TO"
                }
            }
            
        steps{
            echo "Deploying to production"
        }
        }
    }
}
