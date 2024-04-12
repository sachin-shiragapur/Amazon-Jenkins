pipeline {
    agent any
    stages {

        stage('pull') {
            steps {
                git branch: 'main', url: 'https://github.com/PraveenKuber/Amazon-Jenkins.git'
            }
        }

// This is a comment for webhook practice

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
       echo 'Failure in the build'
   }

  }


}
