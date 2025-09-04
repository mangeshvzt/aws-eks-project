pipeline {
    agent any

    stages {
        stage('Run Test Script') {
            steps {
                sh 'bash /home/zignuts/jenkins-test/test.sh'
            }
        }
    }

    post {
        always {
            echo "✅ Pipeline finished (success or failure)"
        }
    }
}
