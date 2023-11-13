pipeline {
	agent {
		docker {
			image 'composer:latest'
		}
	}
	stages {
		stage('Build') {
			steps {
				sh 'composer install'
			}
		}
		stage('Test') {
			steps {
                sh 'php ./vendor/bin/phpunit tests/GumballMachineTest.php'
            }
		}
	}
}
