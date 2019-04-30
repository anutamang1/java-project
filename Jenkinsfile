node('linux'){
    stage('UnitTest')
    {
        sh 'ant -f test.xml -v'
    }
    stage('Build')
    {
        sh 'ant -f build.xml -v'
    }
   
}
