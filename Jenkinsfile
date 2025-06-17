pipeline{
    agent any
    environment{
        DOCKER_CREDS = credentials('docker_creds')
        DOCKER_REPO = 'pavandath510/solo-leveling'

    }
    stages{
        stage('Docker Push')
        steps{
            sh "docker tag -t sololeveling:v4 ${DOCKER_REPO}:v1"
            sh "docker login -u ${DOCKER_CREDS_USR} -p ${DOCKER_CREDS_PSW}"
            sh "docker push ${DOCKER_REPO}:v1"
        }
    }
}
