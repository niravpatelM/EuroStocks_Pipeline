pipeline {
	agent {
		label 'Windows_Node'
	} 
	stages {
		stage('Chekout') {
			steps {
				echo "Compile !!"
				git 'https://github.com/gtlniravpatel/EuroStocks_Pipeline.git'
			}
		}
	
		stage ('directAutosLogin_1748') {
			steps {
					echo "directAutosLogin_1748 Execution Started!!"
					bat 'directAutosLogin_1748.bat'
			}
		}
	
		stage ('euroStocksLoginForgot_1567') {
			steps {
					echo "euroStocksLoginForgot_1567 Execution Started!!"
					bat 'euroStocksLoginForgot_1567.bat'
			}
		}
		
		stage ('euroStocksAddProductBackend_1586') {
			steps {
					echo "euroStocksAddProductBackend_1586 Execution Started!!"
					bat 'euroStocksAddProductBackend_1586.bat'
			}
		}
		
		stage ('euroStocksAddVehicleBackend_1587') {
			steps {
					echo "euroStocksAddVehicleBackend_1587 Execution Started!!"
					bat 'euroStocksAddVehicleBackend_1587.bat'
			}
		}
		
		stage ('FullSuitesExecution Execution') {
			steps {
					echo "FullSuitesExecution Execution Started!!"
					bat 'FullSuitesExecution.bat'
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