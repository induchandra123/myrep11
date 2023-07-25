pipeline {
	agent {
		label {
			label 'master'
			customWorkspace '/mnt/customwsp123'
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
				sh 'git clone https://github.com/induchandra123/webapp.git'
			}
		}
		
		stage ('build stage') {
			steps {
				dir ('/mnt/customwsp133/game-of-life') {
					sh 'clean install'
				}
			}
		}
	}
}
