pipeline {
	agent any
	parameters {
		string { name: 'TARGET_ENV', description : 'where to deploy'}
	}
	environment {
		DEPLOY_TO = "$(TARGET_ENV)"
	}
	stages {
		stage('TEST') {
			when{
				environment name:'DEPLOY_TO', value:"test"
			}
			steps {
				sh '''
					pwd
					sleep 5
					echo This is the fist stage1
					exit 1
				'''
			}
		}

		stage('PROD') {
			when {
				environment name:'DEPLOY_TO', value:"prod"
			}
			steps {
				sh '''
					pwd
					sleep 5
					echo This is the fist stage2
				'''
			}	
		}
	}
}
