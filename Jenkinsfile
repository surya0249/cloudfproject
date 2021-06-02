pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name Vpc-stack --template-body file://vpc  --region 'us-east-2'"
            }
        }
	stage('Submit Stack2') {
            steps {
            sh "aws cloudformation create-stack --stack-name ec2-demo --template-body file://ec2 --parameters ParameterKey=KeyPairName,ParameterValue=terraform-key --region 'us-east-2'"
            }
        }
    }            
}
