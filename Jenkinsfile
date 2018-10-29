pipeline {
    agent any

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
				sh 'buildBase.sh'			               
            }

        }
		
		stage('Build the Chrome'){
            steps{
                
				//Compile maven using the docker file
				sh 'buildChrome.sh'			               
            }

        }
		
		stage('Build Test'){
            steps{
                
				//Compile maven using the docker file
				sh "buildTest.sh"			               
            }

        }
		
		stage('Combine reports'){
            steps{
                
				//Compile maven using the docker file
				sh "combineReports.sh"			               
            }

        }
		
		stage('Tests'){
            steps{
                
				//Compile maven using the docker file
				bat "docker build -t fitnessetests ./test"	               
            }

        }
		
		stage('Tests run'){
            steps{
                
				//Compile maven using the docker file
				sh "runTests.sh"	               
            }

        }
		
		stage('Tests reports'){
            steps{
                
				//Compile maven using the docker file
				sh "htmlReportIndexGenerator.sh"	               
            }

        }
    }
}