node('linux') {  
    stage('Unit-Test'){
        git 'https://github.com/anutamang1/java-project.git'
        sh 'ant -f test.xml -v'
        junit 'reports/result.xml'
    }
    stage('Build') {    
		sh 'ant -f build.xml -v'   
	}
    stage('Deploy') {    
		sh 'aws s3 cp /workspace/java-pipeline/dist/rectangle-${BUILD_NUMBER}.jar s3://testtesttest121212/'
	}
    stage('Report')
	{
		withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'awscredentials', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
    // some 
						sh 'aws cloudformation describe-stack-resources --region us-east-1 --stack-name jenkins1'
}
	}
}
