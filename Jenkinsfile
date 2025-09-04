pipeline {
    agent any

    stages {
        stage('Run Test Script') {
            steps {
                sh '/Users/jenkins/test_script.sh'
            }
        }
    }

    post {
        always {
            echo "✅ Pipeline finished (success or failure)"
        }
    }
}
