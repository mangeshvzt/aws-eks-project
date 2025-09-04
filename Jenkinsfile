pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                sh '/Users/divyesh/Downloads/test1.sh'
            }
        }
    }

    post {
        always {
            echo "✅ Pipeline finished (success or failure)"
        }
    }
}
