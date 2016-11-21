pipeline {
    agent any
    stages {
        stage("build") {
            steps{
              sh 'echo "Start Build"'
              echo 'End Build'
            }
        }
        stage("SkippedStage") {
            when {
                echo "Should I run?"
                return false
            }
            steps {
                script {
                    echo "World"
                    echo "Heal it"
                }

            }
        }
        stage("deploy") {
            steps{
              sh 'echo "Start Deploy"'
              sh 'echo "Deploying..."'
              sh 'echo "End Deploy"'
            }           
        }
    }
    post {
        failure {
            echo "failed"
        }
        success {
            echo "success"
        }
    }
}
