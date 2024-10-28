pipeline {
	agent{
		node{
			label 'docker-agent-new-ubuntu'
		}
	}
	/*triggers{
		pollSCM '* * * * *'
	}*/
	environment{
		SERVER_CREDENTIALS = credentials('my-pipeline-credential')
	}
	//parameters {
	//	choice(name: 'VERSION', choices: ['1.1.0','1.2.0','1.3.0'], description: 'choose the version to be deployed')
	//	booleanParam(name: 'executeTests', defaultValue: true, description: 'whether test phase needs to be executed')
	//}
	stages {
		stage(“build”) {
			steps {
        			echo "building the application"
				echo "application built"
				}
			}
		stage(“test”) {
			/*when{
				expression{
					params.executeTests == true
				}
			}*/
			steps {
				echo "testing the application"
			}
		}
		stage(“deploy”) {
			steps {
				echo "deploying the application"
				//echo "deploying version ${params.VERSION}"
				echo "deploying with ${SERVER_CREDENTIALS}"
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
