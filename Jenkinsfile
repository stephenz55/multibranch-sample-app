pipeline {
  agent {label "windows"}
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
	disableConcurrentBuilds()
  }
  stage {
    stage('Hello') {
	  steps {
	    echo "Hello"
	  }
     }
   } 
}
