pipeline
{
    agent any
    triggers
    {
        pollSCM('* * * * *')
    }
    stages
    {
        stage("Git Checkout")
        {
            steps
            {
                echo "Fetching code from git hub"
                git 'https://github.com/nithin4733/maven_appweb.git'
            }
        }
        stage("mvn validate")
        {
            steps
            {
                bat 'mvn validate'
            }
        }
        stage("mvn compile")
        {
            steps
            {
                bat 'mvn compile'
            }
        }
        stage("mvn test")
        {
            steps
            {
                bat 'mvn test'
            }
        }
        stage("mvn package")
        {
            steps
            {
                bat 'mvn package'
            }
        }
        stage("mvn install")
        {
            steps
            {
                bat 'mvn install'
            }
        }
    }
}
