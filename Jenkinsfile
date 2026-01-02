pipeline{
    agent any
    environment{
        IMAGE_NAME='hothaifa'
        ENV='PROD'
        TAG='${env.BUILD_NUMBER}'
    }

    stages{
        stage("checkout code"){
            steps{
                sh 'echo checking the code'
            }
        }

        stage("build image"){
            steps{
                sh 'sleep 4'
                sh 'echo building image $IMAGE_NAME:v$TAG'
            }
        }

        stage("test"){
            steps{
                sh 'echo unit test '
                sh 'echo generating report '
                sh 'echo push report '
            }
        }
        stage("push image"){
            steps{
                sh "date > file.txt"
                sh "ls "
                sh "echo this is whats uppp"
            }
        }
    }

}