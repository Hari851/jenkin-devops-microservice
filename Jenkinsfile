pipeline {
	//agent any
	agent{docker{image 'maven:3.6.3'}}
	  stages{
		  stage('build'){
			  steps{
				  echo "mvn --version"
               echo "Build"
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
