pipeline{
	agent{
		label{
			label 'built-in'
			customWorkspace '/mnt/custom/'
		}
	}
	
	stages{
		stage('install-httpd'){
			steps{
				sh "yum install httpd -y"
			}
		}
		
		stage('server-start'){
			steps{
				sh "service httpd start"
			}
		}
		
		stage('deploy-index'){
			steps{
				sh "echo 'Hii Bhushan Achat' >> /var/www/html/index.html"
				sh "chmod -R 777 /var"
			}
		}
	}
}
