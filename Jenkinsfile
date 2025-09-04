pipeline {
    agent {
        node {
            label 'any'
            customWorkspace '/home/zignuts/monile-app'
        }
    }

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
