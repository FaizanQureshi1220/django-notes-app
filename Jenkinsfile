@Library('shared_libs') _
pipeline {
    agent {label 'worker-1'}
    
    stages{
        stage("Clone Code"){
            steps{
                script {
                    clone ("https://github.com/FaizanQureshi1220/django-notes-app" , "dev")
                }
            }
        }
        stage("Build and Test"){
            steps{
                script {
                    build ("notes-app" , "latest")
                }
            }
        }
        stage("test"){
            steps{
               echo "this is test"
            }
        }
        stage("Deploy"){
            steps{
                script {
                    compose ()
                }
            }
        }
    }
}
