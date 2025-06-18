pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                echo 'Building the page'
            }
        }
        stage('ParallelStages') {
            parallel {
                stage('CodeAnalysis') {
                    steps {
                        echo "Running Code Analysis"
                    }
                }
                stage('SecurityScan') {
                    steps {
                        echo "Running Security Scan"
                    }
                }
                stage('PerformanceTest') {
                    steps {
                        echo "Running Performance Test"
                    }
                }
            }
        }
    }
}
