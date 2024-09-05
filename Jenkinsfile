pipeline {
    agent any
    stages {
        stage('Parallel Deployments') {
            parallel {
                stage('Deploy Branch 1') {
                    when {
                        branch 'master'
                    }
                    steps {
                        echo 'Deploying code from branch-1...'
                        // Replace with your deployment command
                        sh './deploy.sh master'
                    }
                }
                stage('Deploy Stage') {
                    when {
                        branch 'stage'
                    }
                    steps {
                        echo 'Deploying code from branch-2...'
                        // Replace with your deployment command
                        sh './deploy.sh stage'
                    }
                }
                stage('Deploy dev') {
                    when {
                        branch 'branch-3'
                    }
                    steps {
                        echo 'Deploying code from branch-3...'
                        // Replace with your deployment command
                        sh './deploy.sh dev'
                    }
                }
            }
        }
    }
    post {
        always {
            echo 'Cleaning up after deployment...'
            // Cleanup steps if needed
        }
    }
}
