pipeline {
	agent any
	parameters {
		choice(name: 'TARGET_ENV',choices:['test','prod'], description : 'where to deploy')
	}
	environment {
		DEPLOY_TO = "$TARGET_ENV"
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
					echo "Deploying to test environment"
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
					echo "Deploying to prod environment"
				'''
			}	
		}
	}
}
