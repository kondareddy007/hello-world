pipeline{
    agent any
    environment{
        PATH = "/opt/homebrew/Cellar/maven/3.9.4/libexec/bin:$PATH"
    }
    stages{
        stage('Git Checkout'){
            steps{
                git credentialsId: 'github', url: 'https://github.com/kondareddy007/hello-world.git'
            }
        }
        stage('Maven build'){
            steps{
                sh "mvn clean install"
            }
        }
        
            
        
    }
}
