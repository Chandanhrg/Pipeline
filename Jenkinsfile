pipeline {
  agent none	
  stages {
    stage ('BUILD') {
      agent any
	steps {
        echo "This is Build stage" 
        sh ''' 
		sleep 5
	        exit 0 
	   '''
      }  
    }  
    
    stage ('TEST') {
      agent { label "label1" }
	    steps {
	 echo "This is Test stage" 
        sh 'sleep 5; exit 0'
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
