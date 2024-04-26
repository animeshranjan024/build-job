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
		cron('H(0-1) 1,14 * * *')
	}

	environment {
		DATE = new Date().format('yyyy-mm-dd')
	}

    stages {

    	stage('Update as run') {
    		steps {
    			script {
					echo "Build Id: ${params.RELEASE_NUMBER}.build${env.BUILD_NUMBER}_${env.DATE}"
					currentBuild.displayName = "${params.RELEASE_NUMBER}_${env.BUILD_NUMBER}_${params.ENVIRONMENT}"
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