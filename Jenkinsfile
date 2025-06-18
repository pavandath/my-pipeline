pipeline{
    agent any 
    stages{
        stage ('DeploytoDev'){
            steps{
                echo "Deploying to dev environment"
            }
        stage ('DeploytoProd') {
            when{
                //branch expression
            expression {BRANCH_NAME ==~ /(production|staging)/}     // ==~ matches regular expression if the left  expr matches right
            }                                                       // if the branch is either one from both it will run
            steps{
                echo "Deploying to Production"
            }
            
        }
        }
    }
}
