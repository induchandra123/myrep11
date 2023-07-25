pipeline {
	agent {
		label {
			label 'master'
			customWorkspace '/mnt/customwsp-demo'
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
				dir ('/mnt/customwsp-demo/game-of-life') {
					sh 'mvn clean install'
				}
				
			}
		}
		
	}
}
