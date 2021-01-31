pipeline {
    agent {label 'slave'}
    stages {
        stage('preparation'){
            steps {
                git 'https://github.com/METoubar/Booster_CI_CD_Project.git'
            }
        }

        stage('build'){
            steps {
                sh 'docker-compose up'
            }
        }
    }

    post {
                success {
                slackSend (color: '#00FF00', message: "SUCCESSFUL: Job '${env.JOB_NAME}  [${env.BUILD_NUMBER}]' (${env.BUILD_URL}console)")
                }

                failure {
                slackSend (color: '#FF0000', message: "FAILED: Job '${env.JOB_NAME}  [${env.BUILD_NUMBER}]' (${env.BUILD_URL}console)")
                }

                unstable {
                slackSend (color: '#FDDB3A', message: "Unstable: Job '${env.JOB_NAME}  [${env.BUILD_NUMBER}]' (${env.BUILD_URL}console)")
                }

                aborted {
                slackSend (color: '#000000', message: "ABORTED: Job '${env.JOB_NAME}  [${env.BUILD_NUMBER}]' (${env.BUILD_URL}console)")
                }
            }
}