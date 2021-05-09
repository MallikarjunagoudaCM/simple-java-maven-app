pipeline{
    
    agent none
  
    stages{
        
        stage('SCM') {
            
            agent {
                label "myslavemaven"
                }
          
            steps {
              echo "This is 2nd Br SCM job"
              sh "date"
              
            }
        
        }
        
        stage('Build') {
            
            agent {
                label "myslavemaven"
            }
            steps {
              echo "This is 2nd Br Build job"
            }
        
        }
        
        stage('Deploy') {
            
            agent {
                label "myslavemaven"
            }
            
            steps {
              echo "This is 2nd Br Deploy job"
            }
        
        }
        
    }
    
    
}
