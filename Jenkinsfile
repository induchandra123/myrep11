pipeline {
	agent {
		label {
			label 'master'
			customWorkspace '/mnt/customwsp-demo11'
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
		
		stage ('build') {
		
			steps {
				dir ('/mnt/customwsp-demo11/webapp') {
					sh 'clean install'
				}
				
			}
		}
		
	}
}
