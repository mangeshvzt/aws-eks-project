pipeline {
    agent any

    stages {
        stage('Run Test Script') {
            steps {
                sh 'bash /home/zignuts/tmp/test.sh'
            }
        }
    }

    post {
        always {
            echo "✅ Pipeline finished (success or failure)"
        }
    }
}
