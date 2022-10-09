pipeline{
	agent{
		label{
				label'built-in'
				customWorkspace '/project'
				
		}
	}
	stages{
		stage('install http')
		{
		steps{
		sh "sudo yum install httpd -y"
		sh "sudo service httpd start"
		}
		}
		stage('copy index file')
		{
		steps{
		sh "sudo cp  -r index.html /var/www/html/"
		sh "sudo chmod -R 777 index.html"
		}
		}
	}
}
