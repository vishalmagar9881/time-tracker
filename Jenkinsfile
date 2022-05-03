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
                    sh 'mv /root/.jenkins/workspace/time-tracker-jenkins-pipeline/web/target/time-tracker-web-0.5.0-SNAPSHOT.war /root/apache-tomcat-9.0.62/webapps'
                    sh 'echo "Deployment completed for time-tracker Application....."'
                }
                
            }
        }
    
    
    post {
            success {
                echo "Application successfully deploy in apace tomcat server."
            }
            failure {
                echo "Deployment Failed."
            }
            always {
        // Let's wipe out the workspace before we finish!
                sh 'rm -rf /root/.jenkins/workspace/time-tracker-jenkins-pipeline/*'
                echo "Workspace cleaned"
            }
    }
    
    
    
}
