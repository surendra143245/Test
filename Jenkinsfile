pipeline {

    agent any

    stages {

        stage('Build') {

            steps {

           echo "build"    

                sh "java Hello.java"

            }

        }

        stage('execute') {

            steps {

               echo "test"

                sh "java Hello"

            }

        }

        stage('Deploy') {

            steps {

              echo "deploy"

            }

        }
        stage ('success'){
            steps {
                script {
                    currentBuild.result = 'SUCCESS'
                }
            }
             post {
        failure {
            script {
                currentBuild.result = 'FAILURE'
            }
        }

        always {
            step([$class: 'Mailer',
                notifyEveryUnstableBuild: true,
                notifyEverystableBuild: true,
                recipients: "beeramsurendrareddy@gmail.com",
                sendToIndividuals: true])
        }
    }

    }
    }

}
