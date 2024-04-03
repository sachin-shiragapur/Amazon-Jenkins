pipeline {
    agent {
        label 'Agent windows-vm-public-ip-slave'
    }
      stages { 
          
          stage('pull') {
            steps {
                git branch: 'main', url: 'https://github.com/sachin-shiragapur/Amazon-Jenkins.git'
            }
        }
      
    
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }

          stage('build') {
            steps {
                 sh 'mvn clean install'
            }
        }
      }
    
post{
    
  failure{
       echo 'Failure in the build occurs'
   }     
         
  }
      
}

