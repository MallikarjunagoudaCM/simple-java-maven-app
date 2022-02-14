pipeline{
    
    agent none
  
    stages{
        
        stage('SCM checkout and build') {
            
            agent {
                label "digital_node"
                }
            environment {
                 MAVEN_HOME = "/opt/apache-maven-3.8.4/bin"
            }
          
            steps {
              git "https://github.com/MallikarjunagoudaCM/simple-java-maven-app.git"
              sh "${MAVEN_HOME}/mvn clean package"
              sh 'pwd'
              sshagent(['d23e63f8-c68c-4c29-be87-fe740f5746c4']) {
                
              }
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
