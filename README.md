pipeline
{
    agent any
    stages
    {
        stage('Checkout')
        {
            steps
            {
                git branch:'main',url:'https://github.com/AnnaBinoy09/demo_devops.git';
            }
        }
        stage('Build')
        {
            steps
            {
                sh 'mvn clean package'
            }
        }
        stage('Test')
        {
            steps
            {
                sh 'mvn test'
            }
        }
        
    }
}
