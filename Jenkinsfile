pipeline {
	agent any
	stages {
		stage(“build”) {
			steps {
        			echo "building the application"
				}
			}
		stage(“test”) {
			steps {
				echo "testing the application"
			}
		}
		stage(“deploy”) {
			steps {
				echo "deploying the application"
			}
		}
	}
	post {
		always {
			echo 'build executed'
		}
		success {
			echo 'build succeeded'
		}
		failure {
			echo 'build failed'
		}
	}
}
