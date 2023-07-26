pipeline {
	agent {
		label {
			label 'master'
			customWorkspace '/mnt/customwsp'
		}
		
	}
	
	tools { 
        maven '3.9.3'
    }
	stages {
		stage ('clean workspace') {
			steps {
				cleanWs()
			}
		}
		
		stage ('git-clone') {
			steps {
				sh 'git clone https://github.com/induchandra123/game-of-life.git'
			}
		}
		
		stage ('build') {
		
			steps {
				dir ('/mnt/customwsp/game-of-life') {
					sh 'mvn clean package'
				}
			}
		}
	}
}
			
