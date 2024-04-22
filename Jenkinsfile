pipeline {

	//pararmeter
	parameters{
		string(name: 'RELEASE_NUMBER', defaultValue: '', description: 'Release Number', trim: true)
		string(name: 'ENVIRONMENT', defaultValue:'', description: 'Environment Name', trim: true)
		string(name: 'BRANCH_NAME', defaultValue: '', description: 'Branch Name', trim:true)
	}

	agent any

	option {
		timestamp()
	}

	triggers{
		cron('H(0-1) 9,15 * * *')
	}

	// environment {

	// }

    stages {

    	stage('Update as run') {
    		steps {
    			script {
					echo "Update as run"
				}
    		}
    	}

    	stage('Source Checkout') {
			steps {
				script{
					echo "Source Checkout"
				}
			}
    	}

    	stage('Build') {
			steps {
				script {
					echo "build"
				}
			}
    	}

    	stage('Post Build') {
			steps {
				script {
					echo "Poost build"
				}
			}
    	}

    	stage('Invoke') {
			steps {
				script {
					echo "Invoke"
				}
			}
    	}
    }  
}