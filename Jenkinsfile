pipeline {
	agent {
		label {
			label 'slave-2'
			customWorkspace '/mnt/vikram'
		}
	}
	    stages {
			stage ('git-clone') {
				steps {
					sh "sudo yum install git -y"
					sh "sudo yum install httpd -y"
					sh "git clone https://github.com/kvikram101/vel-app.git"
					sh "cd vel-app && sudo cp -r index.html /var/www/html"
					sh "sudo chmod -R 777 /var/www/html"
					sh "sudo service httpd start"
				}
			}
		}
}

