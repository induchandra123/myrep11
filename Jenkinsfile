pipeline {
	agent {
		label {
			label 'master'
			customWorkspace '/mnt/customwsp-demo13'
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
				dir ('/mnt/customwsp-demo13/webapp') {
					sh 'mvn clean install'
				}
				
			}
		}
		
	}
}
