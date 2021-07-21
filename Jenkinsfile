pipeline {
				agent any 
				stages {
					stage('BUILD') {
						steps {
							sh '''
								pwd
								sleep 5
								echo This is the fist stage: BUILD
							'''
						}	
					}
					
					stage('TEST') {
						parallel {
							stage('TEST1'){
								steps {
									sh '''
										pwd
										sleep 5
										echo This is the TEST1 stage
									'''
								}
							}
							stage('TEST2'){
								steps {
									sh '''
										pwd
										sleep 5
										echo This is the TEST2 stage
									'''
								}
							}
							stage('TEST3'){
								steps {
									sh '''
										pwd
										sleep 5
										echo This is the TEST3 stage
									'''
								}
							}
						}
							
					}
					
					stage('DEPLOY') {
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
