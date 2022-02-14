pipeline{
    
    agent none
  
    stages{
        
        stage('SCM checkout and build') {
            
            agent {
                label "AWS_node"
                }
            environment {
                 MAVEN_HOME = "/opt/apache-maven-3.6.3/bin"
            }
          
            steps {
              git "https://github.com/MallikarjunagoudaCM/simple-java-maven-app.git"
              sh "${MAVEN_HOME}/mvn clean package"
              sh 'pwd'
              /* sshagent(['a6a793f6-2b73-4107-bc3b-39ce4461d106']) {
                 
              } */
            }
        
        }
        /**
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
                docker "mallikarjunagouda/httpd-git"
            }
            
            steps {
              echo "This is Deploy job"
            }
        
        }
        */
    }
    
    
}
