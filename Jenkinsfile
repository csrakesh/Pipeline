pipeline {
				agent any 
				stages {
					/*
					stage('STAGE1') {
						steps {
							catchError(buildResult : 'SUCCESS', stageResult : 'FAILURE'){
								sh '''
									pwd
									sleep 5
									echo This is the fist stage1
									exit 1
								'''
							}
						}
					}
					*/
					
					stage('STAGE2') {
						when {
							branch : 'master'
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
