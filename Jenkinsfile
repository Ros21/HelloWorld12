pipeline {
  agent any
  environment {
   	NEW_VERSION = '1.3.0'
   	SERVER_CREDENTIALS = credentials('783851aa-91fe-4aee-b4e8-d95396aeb4fd')
  }
  stages {
    stage("build") {
    
      steps {
        echo "building the application... "
        echo "building version ${NEW_VERSION} "
      }
    }

    stage("test") {
    	when {
    		expression {
    			BRANCH_NAME =='dev' || BRANCH_NAME == 'master'
    		}
    	}
    
      steps {
        echo "testing the application... "
      }
    }
    
    stage("deploy") {
    
      steps {
        echo "deploying the application... "
        echo "CREDENTIALS: ${SERVER_CREDENTIALS} "
      }
    }  
    }  
}
