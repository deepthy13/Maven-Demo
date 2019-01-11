pipeline 
{
	
    agent any 
    stages 
    {
        stage ('testscm')
		{
        steps 
        { 
            git 'https://github.com/deepthy13/Maven-Demo.git'
        }
		}
        stage ('testbuild')
        {
		steps
        {
           bat 'mvn clean'
           bat 'mvn install' 
        }
		}
        stage ('testdeploy')
        {
		steps 
        {
		    bat 'xcopy /y "C:\\Program Files (x86)\\Jenkins\\workspace\\pipeline4\\multi-module\\webapp\\target\\webapp.war" "C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps"'
        }
		}
    }
}	
