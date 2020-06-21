pipeline {
	agent any
	//agent{Docker{image 'maven:3.6.3'}}
	environment{
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	  stages{
		  stage('Checkout'){
			  steps{
				 //echo "mvn --version"
				  //echo "node --version"
			   sh 'docker --version'
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
		  stage('build docker image'){
			  steps{
				  "docker build -t in28min/currency-exchange-devops:$env.BUILD_TAG"
			  }
			  }
		  stage('push docker image'){
			  steps{
				  script{
					  docker.withRegistry('','dockerhub'){
					  docker.push();
					  docker.push('latest');
				  }
				  } 
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
