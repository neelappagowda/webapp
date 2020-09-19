pipeline {
	agent none
	stages {
	stage ( 'c-project and java' ) {
		parallel {
		stage ('make') {
			agent { label 'c-node' }
			steps {
			  	git 'https://github.com/neelappagowda/c-project_1.git'
					sh 'make'
				echo 'This is slaveforc node with STAGE 1'
						sh 'sleep 10'
			}
		}
		stage ('Java Project') {
			agent { label 'java-node' }
			 tools {
        maven 'Apache Maven 3.0.5' 
    }
			steps {
				 sh 'mvn --version'
				git 'https://github.com/neelappagowda/Test.git'
				sh 'mvn clean install'
			}
		}
		}
	}
		
	}
}
