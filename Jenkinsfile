pipeline {
    agent any
    
    tools{
        maven '3.8.3'
    }
    
    environment {
                SERVICE_BRANCH = "master"
            }
            
    stages {
        stage('checkout') {
            steps {
                echo "the branch is ${params.branch}"
                git branch: 'main', url: 'https://github.com/microdegree-kannada/mvn_jar.git'
                }
            }
        stage('compile and build'){
          
            steps{
                sh "mvn clean install"
                sh 'echo "The environment variable is ${SERVICE_BRANCH}"'
                }
            }
        stage('Test'){
            steps{
              echo "The environment variable is"
             }
        }
    }
    post { 
        always { 
           echo "The environment variable is"
        }
    }
}

