pipeline {
	agent none
	stages {
		stage('Non-Parallel Stage') {
		    agent {
		        label "master"
		    }
			steps {
				echo "This stage will be executed first!!";
				}
			}
			
		stage('Run Test') {
		    parallel {
		        stage ('Test on Ubantu Node 2') {
		            agent {
		                label "Ubantu_Node_2"
		            }
		            steps {
				        echo "Task 1 is on Agnet node ubantu node 2!";
				    }
		        }
		        
		         stage ('Test on Master') {
		            agent {
		                label "master"
		            }
		            steps {
				        echo "Task 1 is on Master node ubantu!";
				    }
		        }
			}
		}
        	
	}
}
