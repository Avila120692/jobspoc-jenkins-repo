pipeline {
  agent {
    node {
      label 'Windows-Node'
    }

  }
  stages {
    stage('Start') {
      steps {
        bat 'echo ***************************************************************'
        bat 'echo Stage : START'
        bat 'echo Im running on Windows!'
		bat 'dir'
      }
    }
    stage('Store') {
      steps {
        bat 'echo *****************************************************************'
        bat 'echo Stage : STORE'
      }
    }
    stage('Archive') {
      steps {
        bat 'echo *****************************************************************'
        bat 'echo Stage : ARCHIVE'
      }
    }
    stage('Execute') {
      steps {
        bat 'echo *****************************************************************'
		bat 'echo Stage : EXECUTE'
        bat 'echo Loading file : "<filename>"'
		bat 'call "hrh2sprod\\job\\HRFidEmpFull\\HRFidEmpFull.cmd"'
      }
    }
	stage('Test') {
      steps {
        bat 'echo *****************************************************************'
        bat 'echo Stage : TEST'
      }
    }
  }
  post {
    always {
      bat 'echo This will always run'

    }

    success {
      bat 'echo This will run only if successful'

    }

    failure {
      bat 'echo This will run only if failed'

    }

    unstable {
      bat 'echo This will run only if the run was marked as unstable'

    }

    changed {
      bat 'echo This will run only if the state of the Pipeline has changed'
      bat 'echo For example, if the Pipeline was previously failing but is now successful'
    }
  }
}