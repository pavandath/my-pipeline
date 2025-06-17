pipeline{
    agent any
    environment{
        DOCKER_CREDS = credentials('docker_creds')
        DOCKER_REPO = 'pavandath510/solo-leveling'

    }
    stages{
        stage('Docker Push') {
        steps{
            sh "docker images"
        }
        }
    }
}
