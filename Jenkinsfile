pipline{
    agent any
    stages{
        stage ('Build'){
            echo "Building the project"
        }
    }
    post{
        success{
            mail bcc: '', body 'Build is success you can deplow now', cc: '', from: '',replyTo:'',subject: 'Jenkins Job status', to: 'pbachala@softility.com'
        }
    }
}
