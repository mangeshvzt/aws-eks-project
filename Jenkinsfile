pipeline {
    agent any

    stages {
        stage('Test') {
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
