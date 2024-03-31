pipeline {
    agent {
        node {
            label linux-private-ip-vm-ssh1-vm3
        }
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
