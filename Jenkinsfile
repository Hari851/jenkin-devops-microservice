pipeline {
	agent any
	  stages{
		  stage('build'){
			  steps{
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


	  }
}
