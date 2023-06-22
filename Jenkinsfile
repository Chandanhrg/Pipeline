pipeline {
  agent none	
  stages {

    stage ('BUILD') {
      steps {
	agent any 
        echo "This is Build stage" 
        sh ''' 
		sleep 5
	        exit 0 
	   '''
      }  
    }  
    
    stage ('TEST') {
      steps {
	agent { label "label1" }
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
