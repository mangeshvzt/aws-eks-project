pipeline {
    agent any

    stages {
        stage('Run Test Script') {
            steps {
                sh 'sudo /Users/divyesh/Downloads/test.sh'
            }
        }
    }

    post {
        always {
            echo "✅ Pipeline finished (success or failure)"
        }
    }
}
