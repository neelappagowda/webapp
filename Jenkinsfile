pipeline {
agent { label 'java-node' }
	stages {
		stage ('test') {
			steps {
				echo 'this is doing test build'
				sh '''
        pwd
					if [[ -d './webapp' ]]; then 
						cd './webapp' && git pull 
					else 
						git clone https://github.com/neelappagowda/Test.git && cd ./webapp
					fi
					mvn clean install
        '''
			}
		}
		stage ('maven package') {
			steps {
		sh '''  pwd
					if [[ -d './webapp' ]]; then 
						cd './webapp' && git pull 
					else 
						git clone https://github.com/neelappagowda/webapp.git && cd ./webapp
					fi
					mvn clean install '''
        }
        }
        }
}
