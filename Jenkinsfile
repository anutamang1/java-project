node('linux'){
    stage('UnitTest')
    {
        git 'https://github.com/anutamang1/java-project.git'
        sh 'ant -f test.xml -v'
    }
    stage('Build')
    {
        sh 'ant -f build.xml -v'
    }
   
}
