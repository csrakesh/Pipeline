pipeline {
				agent any 
				stages {
					stage('STAGE1') {
						catchError(buildResult : 'SUCCESS', stageResult : 'FAILURE'){
							steps {
								sh '''
									pwd
									sleep 5
									echo This is the fist stage1
									exit 1
								'''
							}
						}
					}
					
					stage('STAGE2') {
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
