pipeline {
    agent {
        label 'windows-vm-public-ip-slave'
    }
      stages { 
          
          stage('pull') {
            steps {
                git branch: 'main', url: 'https://github.com/sachin-shiragapur/Amazon-Jenkins.git'
            }
        }
      
    
          stage('build') {
            steps {
                 bat 'mvn clean install'
            }
        }
      }
    
post{
    
  failure{
       echo 'Failure in the build occurs'
   }     
         
  }
      
}

