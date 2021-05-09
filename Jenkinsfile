pipeline{
    
    agent none
  
    stages{
        
        stage('SCM') {
            
            agent {
                label "myslavemaven"
                }
          
            steps {
              echo "This is SCM job"
              sh "date"
              
            }
        
        }
        
        stage('Build') {
            
            agent {
                label "myslavemaven"
            }
            steps {
              echo "This is Build job"
            }
        
        }
        
        stage('Deploy') {
            
            agent {
                label "myslavemaven"
            }
            
            steps {
              echo "This is Deploy job"
            }
        
        }
        
    }
    
    
}
