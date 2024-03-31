pipeline {
    agent any
    stages {

        stage('pull') {
            steps {
                git branch: 'main', url: 'git@github.com:sachin-shiragapur/Amazon-Jenkins' 
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
