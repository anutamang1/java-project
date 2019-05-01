node('linux'){
    stage('UnitTest')
    {
        git 'https://github.com/anutamang1/java-project.git'
        sh 'ant -f test.xml -v' 
        junit 'reports/result.xml'
    }
    stage('Build')
    {
        sh 'ant'
    }
    
}
