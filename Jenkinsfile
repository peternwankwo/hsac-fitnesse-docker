pipeline {
    agent any
	
	tools {
        maven 'maven'
    }
    stages{
        stage('Setup Fitness'){
            steps{
                //bat "mvn clean package"
				
				//Compile maven
				bat "docker build -t mavencompile ."
				
				
				               
            }

        }
    }
}