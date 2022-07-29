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
      stage('ContinuosDeploy')
       {
         echo "Starting Continous Deploy"
           
        deploy adapters: [tomcat9(credentialsId: 'a6359bf9-6e48-4fcb-829b-1b4e9d28ce4a', path: '', url: 'http://172.31.11.197:8080/')], contextPath: 'testapp', war: '**/*.war'
          }
         stage('ContinuosTest')
       {
         echo "Starting Continous Testing"
           git branch: 'main', url: 'https://github.com/hemakumar1980/FunctionalTesting.git'
           sh 'java -jar /home/ubuntu/.jenkins/workspace/ScriptedPipeLine1/testing.war'
        //deploy adapters: [tomcat9(credentialsId: 'a6359bf9-6e48-4fcb-829b-1b4e9d28ce4a', path: '', url: 'http://172.31.11.197:8080/')], contextPath: 'testapp', war: '**/*.war'
          }
       
}
