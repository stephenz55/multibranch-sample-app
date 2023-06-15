pipeline {
  agent {label "Windows"}
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
	disableConcurrentBuilds()
  }
  stages {
    stage('Hello') {
	  steps {
	    echo "Hello World!"
	  }
	}
    stage('for the fix branch') {
        when {
           branch "fix-*" 
	}
	steps {
	sh '''
	  cat README.md
	'''
	}
    }
    stage('for the PR branch') {
        when {
           branch "PR-*" 
	}
	steps {
	  echo "this only runs for the PRs"
	}
    }
  }
}
