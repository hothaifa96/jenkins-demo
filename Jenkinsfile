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
                parallel{
                    stage("testing route53 AAA record"){
                        steps{
                            sh 'echo testingg ......'
                        }
                    }
                    stage("testing route53 lll record"){
                        steps{
                            sh 'echo testingg ......'
                        }
                    }
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
} 