pipeline {
  agent any
  stages {
    stage("build") {
    
      steps {
        echo "building the application... "
      }
    }

    stage("test") {
    
      steps {
        echo "testing the application... "
      }
    }
    
    stage("deploy") {
    
      steps {
        echo "deploying the application... "
      }
    }    
    post {
    	always {
    		echo "Always: Mail to Members"
    	}
    	failure {
    		echo "Failure: Mail to Members"
    	}
    	 success {
    		echo "Success: Mail to Members"
    	}
    }
 }
}
