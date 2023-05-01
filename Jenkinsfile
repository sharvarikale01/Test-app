pipeline {

agent {
			label{
						label 'built-in'
			}
}

stages{
			stage ('install-tree'){
								steps{
											sh "yum install tree -y"
								}
			}
			
			stage ('install-soft-on-172.31.7.193'){
			agent {
						label {
									label "slaves-1"
						}
			}
								steps {
										sh "sudo yum install httpd -y"
										sh "sudo yum install tree -y"
								}
			}
			
			stage ('install-soft-on-172.31.15.170'){
			agent {
						label {
									label "slaves-2"
						}
			}
								steps {
										sh "sudo yum install httpd -y"
										sh "sudo yum install tree -y"
								}
			}
}
}
