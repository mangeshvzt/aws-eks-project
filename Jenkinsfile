pipeline {
    agent any

    stages {
        stage('Run Test Script') {
            steps {
                sh 'test.sh'
            }
        }
    }

    post {
        always {
            echo "✅ Pipeline finished (success or failure)"
        }
    }
}
