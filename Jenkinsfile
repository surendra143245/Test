pipeline {

    agent any

    stages {

        stage('Build') {

            steps {

           echo "build"    

                sh "javac Hello.java"

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

    }

}
