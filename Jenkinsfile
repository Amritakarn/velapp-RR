pipeline{
	agent {
		node {
			label 'built-in'
			customWorkspace '/data/mypipeline-using-scm'
		}
	}
	stages{
		stage('install apche'){
			steps{
				sh "yum install httpd -y" 
			}
		}
		stage('deploy-index'){
			steps{
				sh "cp -r index.html /var/www/html"
				sh "chmod -R 777 index.html"
			}
		}
	
		stage('restart apache'){
			steps{
			sh "service httpd restart"
			}
		
		}
	}
	

}




