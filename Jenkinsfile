pipeline {
	agent {
		label {
			label 'master'
			customWorkspace '/mnt/customwsp11'
		}
	}
	stages {
		stage ('clean workspace') {
			steps {
				cleanWsp()
			}
		}
		
		stage ('clone repository') {
			steps {
			sh 'git clone https://github.com/induchandra123/game-of-life.git'
			}
			
		}
		
	}
}
