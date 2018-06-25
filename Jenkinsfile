pipeline {
    agent {
		node {
			label 'Windows-Node'
		}
	}
    stages {
        stage('Start') {
            steps {
				bat 'ECHO "*****************************************************************"'
				bat 'ECHO "START"'
                bat 'ECHO "Im running on Windows!"'
				bat 'ECHO "-----------------------------------------------------------------"'
				bat 'DIR'
				bat 'ECHO "-----------------------------------------------------------------"'
				bat 'CD "C:\\Jenkins\\workspace\\test-pipeline_master-\\hrh2sprod\\job"'
				bat 'CD'
				bat 'DIR'
            }
        }
		stage('Store') {
            steps {
				bat 'ECHO "*****************************************************************"'
                bat 'ECHO "STORE PROCEDURE"'
            }
        }
		stage('Archive') {
            steps {
				bat 'ECHO "*****************************************************************"'
                bat 'ECHO "ARCHIVING FILES"'
            }
        }
		stage('Execute') {
			steps {
				bat 'ECHO "*****************************************************************"'
				bat 'ECHO "Loading file <filename>"'
			}
		}
    }
    post {
        always {
            bat 'ECHO "This will always run"'
        }
        success {
            bat 'ECHO "This will run only if successful"'
        }
        failure {
            bat 'ECHO "This will run only if failed"'
        }
        unstable {
            bat 'ECHO "This will run only if the run was marked as unstable"'
        }
        changed {
            bat 'ECHO "This will run only if the state of the Pipeline has changed"'
            bat 'ECHO "For example, if the Pipeline was previously failing but is now successful"'
        }
    }
}
