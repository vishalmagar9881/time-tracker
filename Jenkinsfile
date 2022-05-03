pipeline
{
    
    agent any
    
    stages{
        stage("Building maven Project....."){
            steps
                {
                    sh 'mvn install'
                    sh 'echo "Building maven Project completed....."'
                }
                
            }
        stage("Deplying time-tracker Application....."){
            steps
                {
                    sh 'mv /root/.jenkins/workspace/time-tracker/web/target/time-tracker-web-0.5.0-SNAPSHOT.war /root/apache-tomcat-9.0.62/webapps'
                    sh 'echo "Deployment completed for time-tracker Application....."'
                }
                
            }
        }
    
    
    
}
