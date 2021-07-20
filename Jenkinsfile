pipeline {
	agent {label 'slaves'} 
				stages {
					stage('BUILD') {
						when {
							expression {job == 'RUN'}
						}
						steps {
							sh '''
								pwd
								sleep 5
								echo This is the fist stage: BUILD
							'''
						}	
					}
					
					stage('TEST') {
						when {
							expression {job == 'NORUN'}
						}
						steps {
							sh '''
								pwd
								sleep 5
								echo This is the fist stage: TEST
							'''
						}	
					}
					
					stage('DEPLOY') {
						when {
							expression {job == 'RUN'}
						}
						steps {
							sh '''
								pwd
								sleep 5
								echo This is the fist stage: DEPLOY
							'''
						}	
					}
				}
			}
