pipeline {
    parameters {
        string(name: 'DEPLOY_ENV', defaultValue: 'staging', description: '')
    }
    agent any
    stages {
        stage('Test') {
            steps {
                echo "Hello ${params.DEPLOY_ENV}"
                context.log("hahahahahaha")
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
