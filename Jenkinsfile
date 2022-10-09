pipeline{
	agent{
		label{
				label'172.31.32.157'
				customWorkspace '/project'
				
		}
	}
	stages{
		stage('install http')
		{
		steps{
		sh "chmod -R 777 /project"
		sh "sudo yum install httpd -y"
		sh "sudo service httpd start"
		}
		}
		stage('copy index file')
		{
		steps{
		sh "sudo cp  -r index.html /var/www/html/"
		sh "sudo chmod 777 index.html"
		}
		}
	}
}
