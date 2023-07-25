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
	}
}
