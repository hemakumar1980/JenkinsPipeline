node ('built-in')
{
    stage('ContinuosDownload')
       {
         echo "Hello"
             git branch: 'main', url: 'https://github.com/hemakumar1980/maven.git'
          }
        stage('ContinuosBuild')
       {
         echo "Starting Continous Building"
           
          sh 'mvn package'
          }
     
       
}
