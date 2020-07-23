pipeline {
    agent any
    parameters {
        choice(name: 'PLATFORM_FILTER', choices: ['all', 'linux', 'windows', 'mac'], description: 'Run on specific platform')
    }
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
