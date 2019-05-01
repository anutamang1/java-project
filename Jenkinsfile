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
        sh 'aws s3 cp anutamang1/java-project s3:??jenkins/$(JOB_NAME)/$(BUILD_NUMBER)/'
    }
    stage('Report')
    {
        
    }
    
}
 
