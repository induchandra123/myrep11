pipeline {
	agent {
		label {
			label 'master'
			customWorkspace '/mnt/customwsp-demo1'
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
				dir ('/mnt/customwsp-demo1/webapp') {
					sh 'mvn clean install'
				}
				
			}
		}
		
	}
}
