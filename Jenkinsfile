pipeline 
{
    agent any

    stages 
    {
        stage('Build') 
        {
            steps 
            {
                echo 'Build App in development ajay'
                sh 'terraform --version'
                
            }
        }

        stage('Test') 
        {
            steps 
            {
                echo 'Test App in dev'
            }
        }

        stage('Deploy') 
        {
            steps 
            {
                echo 'Deploy App in production'
            }
        }
    }

    post
    {

    	always
    	{
    		emailext body: 'Summary', subject: 'Pipeline Status', to: 'anilkumbala@gmail.com'
    	}

    }
}
