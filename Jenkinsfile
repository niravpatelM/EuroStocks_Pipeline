pipeline {
	agent {
		label 'Windows_Node'
	} 
	stages {
		stage(‘Chekout’) {
			steps {
				echo "Compile !!"
				git 'https://github.com/simplilearn-github/Pipeline_Script.git'
			}
		}
	
		stage (‘Build’) {
			steps {
					echo "JUnit Passed !!"
					bat 'Build.bat'
			}
		}
	
		stage (‘Deploy’) {
			steps {
					echo "Deploy’ Passed !!"
					bat 'Deploy.bat'
			}
		}
		
		stage (‘Test’) {
			steps {
					echo "Deploy’ Passed !!"
					bat 'Unit.bat'
			}
		}
		
		stage (‘Quality’) {
			steps {
					echo "Deploy’ Passed !!"
					bat 'Quality.bat'
			}
		}

	}
	post{
		always{
			echo 'This will always run'
		}
		success{
			echo 'This will run only if success'
		}
		failure{
			echo 'This will run only if failed'
		}
		unstable{
			echo 'This will run only if unstable'
		}
		changed{
			echo 'This will run only if Changes'
			echo 'failure and success now'
		}
	}
}