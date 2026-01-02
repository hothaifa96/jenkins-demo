pipeline{
    agent any

    stages{
        stage("checkout code"){
            steps{
                sh 'echo checking the code'
            }
        }

        stage("build image"){
            steps{
                sh 'echo building image ........'
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