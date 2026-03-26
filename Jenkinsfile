pipeline {
	agent any
	stages {
		stage('Setup') {
			steps {
				echo 'Setting up test environment...'
				sh 'pip3 install pytest --quiet'
			}
		}

		stage('Run Face ID Tests') {
			steps {
				echo 'Running Face ID simulation tests...'
				sh '/Users/larn/Library/Python/3.9/bin/pytest face_id_tests.py -v'
			}
		}
	}

	post {
		success {
			echo 'All Face ID tests passed.'
		}
		failure {
			echo 'One or more Face ID tests failed. Review console output.'
		}
	}
}

