pipeline {
	agent any
	//agent{Docker{image 'maven:3.6.3'}}
	  stages{
		  stage('build'){
			  steps{
				 //echo "mvn --version"
				  //echo "node --version"
               echo "Build"
			   echo "$PATH"
			   echo "$env.BUILD_ID"
			   echo "$env.JOB_NAME"

			  }
			 }
		  stage('test'){
			   steps{
			  echo "Test"
			   }
		  }
		  stage('Integration Test'){
			   steps{
			  echo "Integration Test"
			   }
		  }
	  }

	  post{
        always{
			echo "im cool always"
		}
		success{
			echo "success"
		}
		failure{
			echo "failure"
		}
//changed
//unstable

	  }
}
