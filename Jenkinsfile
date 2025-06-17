pipeline{
    agent any
    //Global env section, it can be used by all stages
    environment {
        course = "Devops with ${pavan}"
        name = "Pavan"
    }
    stages{
        stage ('Build'){
            // this can be used by only this stage
            environment {
                cloud = 'GCP'
            }
            steps{
                echo "Welcome ${name}"
                echo "Thankyou for enrolling ${course}"
                echo "You are certified in ${cloud}"
            }
        }
    }
}
