pipeline {
    agent any
    stages {

        stage('pull') {
            steps {
                git branch: 'main', credentialsId: 'sachin-pipeline1', url: 'https://github.com/sachin-shiragapur/Amazon-Jenkins.git'
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
