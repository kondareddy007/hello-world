pipeline
{
    agent any
    stages
    {
        stage('Git Checkout')
        {
            steps
            {
                git credentialsId: 'github', url: 'https://github.com/kondareddy007/hello-world.git'
            }
        }
        
    }
}
