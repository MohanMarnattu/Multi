pipeline
{
    agent any
     stages
     {
         stage("ContDownload")
         {
            steps
            {
                git 'https://github.com/intelliqittrainings/maven.git'
            }
         }
         
         stage("ContBuild")
         {
             steps
             {
                 sh 'mvn package'
             }
         }
         stage("ContDeployment")
         {
             steps
             {
                 sh 'scp /var/lib/jenkins/workspace/Pipeline/webapp/target/webapp.war ubuntu@172.31.37.153:/var/lib/tomcat9/webapps/prod1.war'
             }
         }
         
     }
         
}
