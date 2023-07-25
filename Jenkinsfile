pipeline {
	agent {
		label {
			label 'master'
			customWorkspace '/mnt/customwsp13'
		}
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
				dir ('/mnt/customwsp13/game-of-life') {
					sh 'mvn clean install'
				}
				
			}
		}
		
	}
}
