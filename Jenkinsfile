pipeline {

	//pararmeter
	parameters{
		string(name: 'RELEASE_NUMBER', defaultValue: '24.1.0', description: 'Release Number', trim: true)
		string(name: 'ENVIRONMENT', defaultValue:'ALPHAQ', description: 'Environment Name', trim: true)
		string(name: 'BRANCH_NAME', defaultValue: 'central', description: 'Branch Name', trim:true)
	}

	agent any

	options {
		timestamps()
	}

	triggers{
		cron('H 1,12 * * *')
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