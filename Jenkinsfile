pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                sh '/Users/divyesh/Downloads/auto-build-flutter.sh'
            }
        }
    }

    post {
        always {
            echo "✅ Pipeline finished (success or failure)"
        }
    }
}
