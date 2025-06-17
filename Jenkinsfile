pipeline{
    agent any
    environment{
        DOCKER_CREDS = credentials('hub_creds')
        DOCKER_REPO = 'pavandath510/solo-leveling'

    }
    stages{
        stage('Docker Push') {
        steps {
                withCredentials([usernamePassword(credentialsId: 'docker_creds', usernameVariable: 'DOCKER_CREDS_USR', passwordVariable: 'DOCKER_CREDS_PSW')]) {
                    sh "docker tag sololeveling:v4 ${DOCKER_REPO}:v1"
                    sh "docker login -u ${DOCKER_CREDS_USR} -p ${DOCKER_CREDS_PSW}"
                    sh "docker push ${DOCKER_REPO}:v1"
                }
        }
        }
    }
}
