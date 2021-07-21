pipeline {
				agent any 
				stages {
					stage('STAGE1') {
						steps {
							sh '''
								pwd
								sleep 5
								echo This is the fist stage: BUILD
								exit 1
							'''
						}	
					}
					
					stage('STAGE2') {
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
