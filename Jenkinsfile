node('linux'){
    stage('Unit Test')
    {
        git 'https://github.com/anutamang1/java-project.git'
        sh 'ant -f test.xml -v' 
        junit 'reports/result.xml'
    } 
    stage('Build')
    {
        sh 'ant -f build.xml -v'
    }
    stage('Deploy')
    {
        sh 'aws s3 cp /workspace/java-pipeline/dist/rectangle-{BUILD_NUMBER}.jar s3://seis665-anutamang/rectangle${BUILD_NUMBER}.jar'
    }
    stage('Report')
    {
        sh 'aws cloudformation describe-stack-resources --region us-east-1 --stack-name jenkins'
    }
    
}
 
