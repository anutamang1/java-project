node('linux'){
    stage('Test')
    {
        git 'https://github.com/anutamang1/java-project.git'
        sh 'ant -buildfile test.xml' 
        junit 'reports/*.xml'
    }
    stage('Build')
    {
        sh 'ant'
    }
   
}
