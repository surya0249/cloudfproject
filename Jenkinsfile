pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name ec2-stack --template-body file://ec2   --parameters  ParameterKey=KeyName,ParameterValue=terraform-key --region 'us-east-2'"
            }
        }
	
    }            
}
