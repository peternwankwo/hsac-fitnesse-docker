pipeline {
    agent any
	
	tools {
        maven 'maven'
    }
    stages{
        stage('Setup and compile Maven'){
            steps{
                
				//Compile maven using the docker file
				bat "docker build -t mavencompile ."			               
            }

        }
		
		stage('Build the base'){
            steps{
                
				//Compile maven using the docker file
				bat "buildBase.sh"			               
            }

        }
		
		stage('Build the Chrome'){
            steps{
                
				//Compile maven using the docker file
				bat "buildChrome.sh"			               
            }

        }
		
		stage('Build Test'){
            steps{
                
				//Compile maven using the docker file
				bat "buildTest.sh"			               
            }

        }
    }
}