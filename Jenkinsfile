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
                sh 'echo building image $IMAGE_NAME:v$TAG'
            }
        }
        post{
        success{
            sh 'echo push it '
        }
        failure{
            sh 'docker rm -f jenk'
        }
    }

        stage("test"){ // unit ,system, integration,penmtraition, sanity
           parallel{
            stage("unit test"){
                steps{
                    sh 'echo unit'
                }
            }
            stage("system test"){
                steps{
                    sh 'echo system'
                }
            }
            stage("integration test"){
                steps{
                    sh 'echo inte'
                }
            }
            stage("penetaration test "){
                steps{
                    sh 'echo fgdsaf'
                }
            }
            stage("sanity test"){
                steps{
                    sh 'echo san'
                }
            }
            stage("smoke test"){
                steps{
                    sh 'echo smoke'
                }
            }
           }
        }

        stage("push image"){
            steps{
               
                    sh 'echo apply'
                
               }
            }
    }
    post{
        success{
            sh 'echo build passed'
        }
        failure{
            sh 'echo failure '
        }
    }
} 