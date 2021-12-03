pipeline {
    agent {
        label 'master'
        tools{
               maven 'apache-maven_3_8_0'
    }
    
    stages {
        stage('Verify Branch'){
            steps{
                echo "@GIT_BRANCH"
            }
        }
        
        stage('Checkout') {
            steps{
                git branch: 'main', url: 'https://github.com/PKOTHAWA/Newspaperadvertise.git'
            }
        }
    
                stage('Build') {
                    steps{
                        bat 'mvn compile'

                   }
                }
                
                stage('Test') {
                    steps{
                        bat 'mvn test'
                   }
               }
            
                stage('Package') {
                    steps{
                        bat 'mvn package'
                   }
               }
    }
}
