pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                sh '/Users/divyesh/Downloads/test.sh'
            }
        }
    }

    post {
        always {
            echo "✅ Pipeline finished (success or failure)"
        }
    }
}
