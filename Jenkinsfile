pipeline {
    parameters {
        string(name: 'DEPLOY_ENV', defaultValue: 'staging', description: '')
    }
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'echo "Fail!"; exit1'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will only run if success'
        }
        failure {
            echo 'This will always run if failed'
        }
    }
}
