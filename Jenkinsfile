pipeline{
    agent any
    tools {
        terraform 'TERRAFORM_HOME'
    }
    stages{
        stage('initialize'){
            steps{
                sh 'terraform init --reconfigure'
            }
        }
        stage('plan'){
            steps{
                sh 'terraform plan'
            }
        }
        stage('apply'){
            steps{
                withAWS(credentials: , region: ){

                        sh 'terraform apply -auto-approve'
                }
                
            }
        }
    }





}