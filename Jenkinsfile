pipeline{
    
    agent none
  
    stages{
        
        stage('SCM') {
            
            agent {
                label "AWS_node"
                }
          
            steps {
              echo "This is SCM job"
              sh "date"
              
            }
        
        }
        
        stage('Build') {
            
            agent {
                label "digital_node"
            }
            steps {
              echo "This is Build job"
            }
        
        }
        
        stage('Deploy') {
            
            agent {
                label "docker"
            }
            
            steps {
              echo "This is Deploy job"
            }
        
        }
        
    }
    
    
}
