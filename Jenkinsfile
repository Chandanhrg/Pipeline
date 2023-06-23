pipeline {
  agent any	
  stages {
    stage ('BUILD') {
     	steps {
        echo "This is Build stage" 
        sh ''' 
		sleep 5
	        exit 0 
	   '''
      }  
    }  
    
    stage ('TEST PARALLEL') {
	parallel {
		stage ('TEST ON CHROME') { 
     	    steps {
		echo "This is Test on chrome" 
       		sh 'sleep 5; exit 0'
		}
		}
		stage ('TEST ON SAFARI') { 
     	    steps {
		echo "This is Test on safari" 
       		sh 'sleep 5; exit 0'
		}
		}
      }  
    }  
    
    stage ('DEPLOY') {
	      steps {
        echo "This is Deploy stage" 
        sh 'sleep 5'
      }  
    }  
  } 
}
